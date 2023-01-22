```php
<?php

namespace vladutt;

class Me extends Developer
{
    public function getInformation(): array {
        return [
            'name' => 'Ilie',
            'surname' => 'Vladut Teodor',
            'age' => 26,
            'company' => 'Auto Magic Cast SRL'
        ];
    }

    public function getKnowledge(): array {
        return [
            Php::class,
            Laravel::class,
            MySQL::class,
            Git::class,
            JavaScript::class,
            Vue::class,
            Nuxt::class,
            EcommercePlatforms::class,
            Docker::class,
            AWS::class,
            ElasticSearch::class,
            Redis::class,
            Mongodb::class,
            RabbitMQ::class,
            Nginx::class,
            Apache::class
        ];
    }

    public function getLatestJobs(): array {
        return [
            'freelancer' => ['from' => 2017, 'to' => 2019],
            'vlinde_transilvania' => ['from' => 2019, 'to' => 2020], // My first job as a real programmer
            'ibsell_net' => ['from' => 2020, 'to' => 2020], // just 2 months - very bad team
            'retargeting' => ['from' => 2020, 'to' => 2022], // an awesome place to work with nice ppl and a very good team
            'pentest_tools' => ['from' => 2022, 'to' => now()], // nice place to work
            'stefanini' => ['from' => 2022, 'to' => now()], // well paied :)
        ];
    }
}

foreach ((new Me())->getLatestJobs() as $name => $period) {
    echo '<b>' . $name. '</b> : ' . 'from ' . $period['from'] . ' to ' . $period['to'] . '<br>';
}

// Output:
```

<b>Freelancer</b>: from 2017 to 2019 <br>
<b>Vlinde Transilvania</b>: from 2019 to 2020 <br>
<b>IBSell net</b>: from 2020 to 2020 <br>
<b>Retargeting</b>: from 2020 to 2022 <br>
<b>Pentest Tools</b>: from 2022 to present <br>
<b>Stefanini</b>: from 2022 to present <br>

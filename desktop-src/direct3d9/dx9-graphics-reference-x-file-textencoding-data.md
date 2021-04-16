---
description: Datenobjekte enthalten die eigentlichen Daten oder einen Verweis auf diese Daten. Jedes Datenobjekt verfügt über eine entsprechende Vorlage, die den Datentyp angibt. In den folgenden Abschnitten werden das Formular und Teile von Datenobjekten erläutert.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Daten (X-Dateiformat, Text Codierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1af117a0207ce804ccacd397bb990fe5f43c94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392698"
---
# <a name="data-x-file-format-text-encoding"></a>Daten (X-Dateiformat, Text Codierung)

Datenobjekte enthalten die eigentlichen Daten oder einen Verweis auf diese Daten. Jedes Datenobjekt verfügt über eine entsprechende Vorlage, die den Datentyp angibt. In den folgenden Abschnitten werden das Formular und Teile von Datenobjekten erläutert.

## <a name="form-identifier-and-name"></a>Formular, Bezeichner und Name

Datenobjekte weisen die folgende Form auf:


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



Der Bezeichner ist obligatorisch und muss mit einem zuvor definierten Datentyp oder primitiven identisch sein. Der Name ist jedoch optional.

## <a name="data-members"></a>Datenelemente

Datenmember können eines der folgenden sein: Datenobjekt, Daten Verweis, ganzzahlige Liste, float-Liste oder Zeichen folgen Liste.

Bei einem Datenobjekt handelt es sich um ein Datenobjekt. Dadurch kann die hierarchische Natur des Datei Formats ausgedrückt werden. Die in der Hierarchie zulässigen Typen von in der-Hierarchie zulässigen Datenobjekten sind möglicherweise eingeschränkt.

Ein Daten Verweis ist ein Verweis auf ein zuvor angetretene Datenobjekt, wie im folgenden Beispiel gezeigt.


```
{
  name |
  UUID |
  name UUID
}
```



Eine ganzzahlige Liste ist eine durch Semikolons getrennte Liste mit ganzen Zahlen, wie im folgenden Beispiel gezeigt.


```
1; 2; 3;
```



Eine float-Liste ist eine durch Semikolons getrennte Liste von Gleit Komma Zahlen, wie im folgenden Beispiel gezeigt.


```
1.0; 2.0; 3.0;
```



Eine Zeichen folgen Liste ist eine durch Semikolons getrennte Liste von Zeichen folgen, wie im folgenden Beispiel gezeigt.


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Text Codierung](text-encoding.md)
</dt> </dl>

 

 




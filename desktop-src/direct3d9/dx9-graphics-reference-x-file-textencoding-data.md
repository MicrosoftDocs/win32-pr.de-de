---
description: Datenobjekte enthalten die tatsächlichen Daten oder einen Verweis auf diese Daten. Jedes Datenobjekt verfügt über eine entsprechende Vorlage, die den Datentyp angibt. In den folgenden Abschnitten werden die Form und Teile von Datenobjekten erläutert.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Daten (X-Dateiformat, Textcodierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acd4222e2878b882b8777e3ba22e28f2d213fb5f3550686baf29b4ed6719e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730201"
---
# <a name="data-x-file-format-text-encoding"></a>Daten (X-Dateiformat, Textcodierung)

Datenobjekte enthalten die tatsächlichen Daten oder einen Verweis auf diese Daten. Jedes Datenobjekt verfügt über eine entsprechende Vorlage, die den Datentyp angibt. In den folgenden Abschnitten werden die Form und Teile von Datenobjekten erläutert.

## <a name="form-identifier-and-name"></a>Formular, Bezeichner und Name

Datenobjekte haben das folgende Formular.


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



Der Bezeichner ist nicht eindeutig und muss mit einem zuvor definierten Datentyp oder primitiven Datentyp übereinstimmen. Der Name ist jedoch optional.

## <a name="data-members"></a>Datenelemente

Datenmitglieder können eines der folgenden Sein: Datenobjekt, Datenverweis, ganzzahlige Liste, Float-Liste oder Zeichenfolgenliste.

Ein Datenobjekt ist ein geschachtelte Datenobjekt. Dadurch kann die hierarchische Natur des Dateiformats ausgedrückt werden. Die in der Hierarchie zulässigen Typen von geschachtelten Datenobjekten können eingeschränkt sein.

Ein Datenverweis ist ein Verweis auf ein zuvor gefundenes Datenobjekt, wie im folgenden Beispiel gezeigt.


```
{
  name |
  UUID |
  name UUID
}
```



Eine ganzzahlige Liste ist eine durch Semikolons getrennte Liste von ganzen Zahlen, wie im folgenden Beispiel gezeigt.


```
1; 2; 3;
```



Eine float-Liste ist eine durch Semikolons getrennte Liste von Floats, wie im folgenden Beispiel gezeigt.


```
1.0; 2.0; 3.0;
```



Eine Zeichenfolgenliste ist eine durch Semikolons getrennte Liste von Zeichenfolgen, wie im folgenden Beispiel gezeigt.


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textcodierung](text-encoding.md)
</dt> </dl>

 

 




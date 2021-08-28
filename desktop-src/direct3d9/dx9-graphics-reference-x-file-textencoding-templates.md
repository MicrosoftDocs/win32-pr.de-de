---
description: Vorlagen definieren, wie der Datenstrom interpretiert wird. Die Daten werden durch die Vorlagendefinition moduliert. In diesem Abschnitt werden die folgenden Aspekte einer Vorlage erläutert, und es wird eine Beispielvorlage angezeigt.
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Vorlagen (X-Dateiformat, Textcodierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e164b92c6c5738ad98b138941b1b2fda6c332068
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881025"
---
# <a name="templates-x-file-format-text-encoding"></a>Vorlagen (X-Dateiformat, Textcodierung)

Vorlagen definieren, wie der Datenstrom interpretiert wird. Die Daten werden durch die Vorlagendefinition moduliert. In diesem Abschnitt werden die folgenden Aspekte einer Vorlage erläutert, und es wird eine Beispielvorlage angezeigt.

Es gibt eine spezielle Vorlage: die Headervorlage. Es wird empfohlen, dass jede Anwendung eine Headervorlage definiert und zum Definieren anwendungsspezifischer Informationen verwendet, z. B. Versionsinformationen. Falls vorhanden, wird dieser Header von der X-Dateiformat-API gelesen. Wenn ein Flags-Member verfügbar ist, wird er verwendet, um zu bestimmen, wie die folgenden Daten interpretiert werden. Der Flags-Member sollte ein DWORD sein, sofern dieser definiert ist. Derzeit ist ein Bit definiert: Bit 0. Wenn dieses Bit klar ist, sind die folgenden Daten in der Datei binär. Wenn diese Einstellung festgelegt ist, sind die folgenden Daten text. Sie können mehrere Headerdatenobjekte verwenden, um zwischen Binärdatei und Text in der Datei zu wechseln.

## <a name="template-form-name-and-uuid"></a>Vorlagenformular, Name und UUID

Eine Vorlage hat das folgende Format.


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



Der Vorlagenname ist ein alphanumerischer Name, der den Unterstrich ( ) enthalten \_ kann. Er darf nicht mit einer Ziffer beginnen. Die UUID ist ein universell eindeutiger Bezeichner, der im Distributed Computing Environment-Standard der Open Software Foundation formatiert und in spitzen Klammern (< >) eingeschlossen ist. Beispiel: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.

## <a name="template-members"></a>Vorlagenmember

Vorlagenmember bestehen aus einem benannten Datentyp gefolgt von einem optionalen Namen oder einem Array eines benannten Datentyps. Gültige primitive Datentypen werden in der folgenden Tabelle definiert.



| type    | Size                               |
|---------|------------------------------------|
| WORD    | 16 Bit                            |
| DWORD   | 32 Bit                            |
| GLEITKOMMAZAHL   | IEEE float                         |
| Double  | 64 Bit                            |
| CHAR    | 8 Bit                             |
| UCHAR   | 8 Bit                             |
| BYTE    | 8 Bit                             |
| STRING  | NULL-terminierte Zeichenfolge             |
| CSTRING | Formatierte C-Zeichenfolge (nicht unterstützt) |
| UNICODE | Unicode-Zeichenfolge (nicht unterstützt)     |



 

Auf zusätzliche Datentypen, die durch Vorlagen definiert werden, die zuvor im Datenstrom aufgetreten sind, kann auch innerhalb einer Vorlagendefinition verwiesen werden. Vorwärtsverweise sind nicht zulässig.

Jeder gültige Datentyp kann in der Vorlagendefinition als Array ausgedrückt werden. Die grundlegende Syntax wird im folgenden Beispiel gezeigt.


```
array <data-type> <name>[<dimension-size>];
```



&lt;dimension-size &gt; kann entweder eine ganze Zahl oder ein benannter Verweis auf ein anderes Vorlagenmember sein, dessen Wert dann ersetzt wird. Arrays können n-dimensional sein, wobei n durch die Anzahl von eckigen Klammern bestimmt wird, die der Anweisung nachgestellt sind, wie im folgenden Beispiel.


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a>Vorlageneinschränkungen

Vorlagen können geöffnet, geschlossen oder eingeschränkt sein. Diese Einschränkungen bestimmen, welche Datentypen in der unmittelbaren Hierarchie eines von der Vorlage definierten Datenobjekts angezeigt werden können. Eine geöffnete Vorlage weist keine Einschränkungen auf, eine geschlossene Vorlage lehnt alle Datentypen ab, und eine eingeschränkte Vorlage lässt eine benannte Liste von Datentypen zu.

Die Syntax zum Angeben einer geöffneten Vorlage besteht aus drei Perioden, die von eckigen Klammern eingeschlossen sind.


```
[ ... ]
```



Eine durch Trennzeichen getrennte Liste benannter Datentypen gefolgt von optionalen UUIDs in eckigen Klammern gibt eine eingeschränkte Vorlage an.


```
[ { data-type [ UUID ] , } ... ]
```



Das Fehlen einer der oben genannten Angaben weist auf eine geschlossene Vorlage hin.

## <a name="template-example"></a>Vorlagenbeispiel

Im Folgenden finden Sie eine Beispielvorlage.


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textcodierung](text-encoding.md)
</dt> </dl>

 

 




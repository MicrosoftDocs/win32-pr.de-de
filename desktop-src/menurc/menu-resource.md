---
title: Menü Ressource
description: Definiert den Inhalt einer Menü Ressource. | Menü Ressource
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- Menü Ressourcen Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350644"
---
# <a name="menu-resource"></a>Menü Ressource

Definiert den Inhalt einer Menü Ressource. Eine Menü Ressource ist eine Auflistung von Informationen, die das Aussehen und die Funktion eines Anwendungs Menüs definiert. Ein Menü ist ein spezielles Eingabe Tool, mit dem ein Benutzer Befehle auswählen und Untermenüs aus einer Liste von Menü Elementen öffnen kann.

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*MENUID*
</dt> <dd>

Die Zahl, die das Menü angibt. Dieser Wert ist entweder eine eindeutige Zeichenfolge oder eine eindeutige 16-Bit-Ganzzahl ohne Vorzeichen im Bereich von 1 bis 65.535.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*
</dt> <dd>

Dieser Parameter kann NULL von mehreren der folgenden Anweisungen sein.



| -Anweisung.                                                        | BESCHREIBUNG                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Merkmale**](characteristics-statement.md) *DWORD*     | Benutzerdefinierte Informationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben. Weitere Informationen finden Sie unter [**Merkmale**](characteristics-statement.md). |
| [**Sprach**](language-statement.md) *Sprache*, *unter Sprache* | Sprache für die Ressource. Weitere Informationen finden Sie unter [**Sprache**](language-statement.md).                                                                                            |
| [**Version**](version-statement.md) *DWORD*                     | Eine benutzerdefinierte Versionsnummer für die Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben. Weitere Informationen finden Sie unter [**Version**](version-statement.md).              |



 

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="examples"></a>Beispiele

Im folgenden finden Sie ein Beispiel für eine Complete **Menu** -Anweisung:

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Menüs](./using-menus.md)
</dt> <dt>

[**Accelerators**](accelerators-resource.md)
</dt> <dt>

[**Charakteristik**](characteristics-statement.md)
</dt> <dt>

[**Kurse**](language-statement.md)
</dt> <dt>

[**Menuex**](menuex-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> <dt>

[**Up**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 

---
description: ICE14 überprüft die Funktions Tabelle einer Windows Installer Datenbank.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346328"
---
# <a name="ice14"></a>ICE14

ICE14 überprüft Folgendes für die Features:

-   Für diese übergeordneten Stamm Funktionen ist das msidbfeatureattributesfollowparent-Bit nicht in der Attribute-Spalte der [Funktions Tabelle](feature-table.md)festgelegt. Eine Stamm Funktion verfügt über kein übergeordnetes Element.
-   Diese Funktion enthält nicht denselben Eintrag in den \_ übergeordneten Spalten des Features und Features der [Funktions Tabelle](feature-table.md). Keine Funktion kann ein eigenes übergeordnetes Element sein.

## <a name="result"></a>Ergebnis

ICE14 gibt eine Fehlermeldung aus, wenn eine Funktion mit dem msidbfeatureattributesfollowparent-Bit festgelegt wurde, oder eine Funktion mit identischen Einträgen in den übergeordneten Spalten der Funktion und der Funktion \_ der Featuretabelle.

## <a name="example"></a>Beispiel

ICE14 gibt die folgenden Fehler für das folgende Beispiel zurück:

-   Die Funktion "Sport" hat denselben Wert in den übergeordneten Spalten der Funktion und des Features der \_ Dateitabelle.
-   Das "msidbfeatureattributesfollowparent"-Bit ist für die Hauptfunktion "Sport" festgelegt.

In der Funktionsstruktur dieses Beispiels ist Sport das Stamm Feature und ein übergeordnetes Element der Features "Swimming" und "Football". Freestyle ist ein untergeordnetes Feature von Swimming. Touchfootball ist ein untergeordnetes Feature von Fußball.

[Funktions Tabelle](feature-table.md) (partiell)



| Funktion       | Attribute | Über \_ geordnetes Element |
|---------------|------------|-----------------|
| Sport         | 4          | Sport           |
| Innenpool      | 1          | Sport           |
| Verbandes      | 4          | Sport           |
| Frei     | 1          | Innenpool        |
| Touchfootball | 4          | Verbandes        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




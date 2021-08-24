---
description: ICE14 überprüft die Featuretabelle einer Windows Installer-Datenbank.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a0789b7844fcbee52654d29b700b167a073fa51778ef3882b1fcbe2864fbb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638170"
---
# <a name="ice14"></a>ICE14

ICE14 überprüft Folgendes auf Features:

-   Für diese übergeordneten Stammfunktionen ist das Bit msidbFeatureAttributesFollowParent in der Spalte Attribute der [Featuretabelle nicht festgelegt.](feature-table.md) Ein Stammfeature verfügt nicht über ein übergeordnetes Element.
-   Diese Funktion verfügt nicht über den gleichen Eintrag in den Spalten Feature und Feature \_ Parent der [Featuretabelle](feature-table.md). Kein Feature kann ein eigenes übergeordnetes Element sein.

## <a name="result"></a>Ergebnis

ICE14 gibt eine Fehlermeldung aus, wenn ein Stammfeature mit dem Bitsatz msidbFeatureAttributesFollowParent oder ein Feature mit identischen Einträgen in den Spalten Feature und Übergeordnetes Feature der Tabelle Feature gefunden \_ wird.

## <a name="example"></a>Beispiel

ICE14 würde die folgenden Fehler für das folgende Beispiel zurückgeben:

-   Das Feature Sport hat den gleichen Wert in den Spalten Feature und Feature \_ Parent der Tabelle File.
-   Für das Stammfeature Sport ist das Bit msidbFeatureAttributesFollowParent festgelegt.

In der Featurestruktur dieses Beispiels ist Sport das Stammfeature und ein übergeordnetes Element der Features "Sport" und "Football". "Free" ist ein untergeordnetes Merkmal von "Child". TouchFootball ist ein untergeordnetes Feature von Football.

[Featuretabelle](feature-table.md) (partiell)



| Feature       | Attribute | Übergeordnetes \_ Feature |
|---------------|------------|-----------------|
| Sport         | 4          | Sport           |
| Schwimmen      | 1          | Sport           |
| Fußball      | 4          | Sport           |
| Freestyle     | 1          | Schwimmen        |
| TouchFootball | 4          | Fußball        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




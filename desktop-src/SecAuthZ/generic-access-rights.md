---
description: Sicherungs fähige Objekte verwenden ein Zugriffs Masken Format, in dem die vier allgemeinen Bits allgemeine Zugriffsrechte angeben.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Generische Zugriffsrechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758250"
---
# <a name="generic-access-rights"></a>Generische Zugriffsrechte

Sicherungs fähige Objekte verwenden ein [Zugriffs Masken Format](access-mask-format.md) , in dem die vier allgemeinen Bits allgemeine Zugriffsrechte angeben. Jeder Typ von Sicherungs fähigen Objekten ordnet diese Bits einem Satz von Standard-und Objekt spezifischen Zugriffsrechten zu. Ein Windows-Datei Objekt ordnet z. b. das generische \_ Lesebit dem Lese Steuerelement zu \_ und synchronisiert Standard Zugriffsrechte und die Datei \_ \_ Daten lesen, Datei \_ Lese \_ -EA und Datei \_ Lese \_ Attribute objektspezifische Zugriffsrechte. Andere Objekttypen ordnen das generische \_ Lesebit jedem beliebigen Satz von Zugriffsrechten zu, der für diesen Objekttyp geeignet ist.

Sie können generische Zugriffsrechte verwenden, um den Typ des Zugriffs anzugeben, den Sie benötigen, wenn Sie ein Handle für ein Objekt öffnen. Dies ist in der Regel einfacher, als alle entsprechenden Standard-und spezifischen Rechte anzugeben.

In der folgenden Tabelle sind die für die generischen Zugriffsrechte definierten Konstanten aufgeführt.



| Konstante         | Generische Bedeutung            |
|------------------|----------------------------|
| generisch \_ alle     | Alle möglichen Zugriffsrechte |
| generisch \_ Ausführen | Zugriff ausführen             |
| generischer \_ Lesevorgang    | Lesezugriff                |
| generischer \_ Schreibvorgang   | Schreibzugriff               |



 

Anwendungen, die private Sicherungs fähige Objekte definieren, können auch die generischen Zugriffsrechte verwenden.

 

 




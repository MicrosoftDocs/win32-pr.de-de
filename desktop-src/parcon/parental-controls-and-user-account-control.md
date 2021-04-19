---
description: Eltern Steuerelemente und Benutzerkontensteuerung
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: Eltern Steuerelemente und Benutzerkontensteuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349203"
---
# <a name="parental-controls-and-user-account-control"></a>Eltern Steuerelemente und Benutzerkontensteuerung

Die Benutzerkontensteuerung (User Account Control, UAC) führt zur Anwesenheit geschützter Administrator-und Standard Benutzerkonten. Ein geschützter Administrator wird mit denselben Rechten wie ein Standard Benutzer unter normaler Auslastung ausgeführt. Für privilegierte Vorgänge:

-   Ein Standard Benutzer wird im Dialogfeld Anmelde Informationen-Benutzeroberfläche angezeigt, in dem die Eingabe eines Benutzernamens und eines Kennworts für einen geschützten Administrator oder einen integrierten Administrator erforderlich ist.
-   Ein geschützter Administrator wird dem Dialogfeld Benutzeroberfläche zustimmen angezeigt, in dem die Option zum Fortfahren ausgewählt werden muss.

Beachten Sie, dass die UAC pro Prozess implementiert ist, sodass ein Prozess entweder mit erhöhten Rechten ausgeführt wird. Im Allgemeinen ist es aus Sicherheitssicht nicht geeignet, große Anwendungen wie immer erweitert auszuführen. Für Eltern Steuerelemente sollte Code, der die Einstellungen ändern muss, durch eine von zwei Implementierungs Optionen isoliert werden:

1.  Erstellen Sie eine kleine ausführbare Datei für die Einstellungs Verwaltung, die in ihrem Manifest als Administratorrechte gekennzeichnet ist. Der Aufruf der ausführbaren Datei bewirkt, dass die Benutzeroberfläche für die Zustimmung oder die Anmelde Informationen angezeigt wird, bevor der Prozess ausgeführt werden kann.
2.  Bereitstellen von COM-Schnittstellen in einer Produkt-dll, die Aufrufe pro UAC-Dokumentation ermöglichen. Dies führt auch dazu, dass die entsprechende Benutzeroberfläche für Zustimmung oder Anmelde Informationen angezeigt wird.

 

 




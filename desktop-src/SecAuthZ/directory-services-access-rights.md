---
description: Jedem Active Directory Objekt ist eine Sicherheits Beschreibung zugewiesen.
ms.assetid: 2e4ed13f-f09e-43b4-9862-95a79c229f0c
title: Zugriffsrechte für Verzeichnisdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f24e75db6733a8f5833e7f45ab5a52dafd67f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218193"
---
# <a name="directory-services-access-rights"></a>Zugriffsrechte für Verzeichnisdienste

Jedem Active Directory Objekt ist eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) zugewiesen. Eine Reihe von Vertrauens rechten für Verzeichnisdienst Objekte kann innerhalb dieser Sicherheits Deskriptoren festgelegt werden. Diese Rechte sind in der folgenden Tabelle aufgeführt. Weitere Informationen finden Sie unter [Steuern von Zugriffsrechten](/windows/desktop/AD/control-access-rights).



| Rechte                                | Bedeutung                                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| actrl- \_ DS \_ geöffnet<br/>            | Öffnen Sie ein DS-Objekt.<br/>                                                                                                                                                                                                                                                            |
| actrl DS untergeordnetes Element \_ \_ Erstellen \_<br/>   | Erstellen Sie ein untergeordnetes DS-Objekt.<br/>                                                                                                                                                                                                                                                    |
| actrl DS untergeordnetes Element \_ \_ Löschen \_<br/>   | Löschen Sie ein untergeordnetes DS-Objekt.<br/>                                                                                                                                                                                                                                                    |
| actrl \_ DS- \_ Liste<br/>            | Enumerieren eines DS-Objekts.<br/>                                                                                                                                                                                                                                                       |
| actrl \_ DS \_ Lese- \_ Prop<br/>      | Lesen Sie die Eigenschaften eines DS-Objekts.<br/>                                                                                                                                                                                                                                          |
| actrl \_ DS- \_ Schreib \_ Prop<br/>     | Schreiben von Eigenschaften für ein DS-Objekt.<br/>                                                                                                                                                                                                                                            |
| actrl \_ DS \_ selbst<br/>            | Der Zugriff ist nur zulässig, nachdem überprüfte Rechte überprüft wurden, die vom-Objekt unterstützt werden Dieses Flag kann allein verwendet werden, um alle validierten Rechte Prüfungen des Objekts auszuführen, oder es kann mit einem Bezeichner eines bestimmten validierten rechts kombiniert werden, um nur diese Überprüfung auszuführen.<br/> |
| actrl \_ DS- \_ Lösch Struktur \_<br/>    | Löschen Sie eine Struktur von DS-Objekten.<br/>                                                                                                                                                                                                                                                 |
| actrl \_ DS- \_ Listen \_ Objekt<br/>    | Auflisten einer Struktur von DS-Objekten.<br/>                                                                                                                                                                                                                                                   |
| actrl \_ DS- \_ Steuerungs \_ Zugriff<br/> | Der Zugriff ist nur zulässig, nachdem von dem-Objekt unterstützte erweiterte Rechte überprüft wurden. Dieses Flag kann allein verwendet werden, um alle erweiterten Rechte Prüfungen für das Objekt auszuführen, oder es kann mit einem Bezeichner eines bestimmten erweiterten Rechts kombiniert werden, um nur diese Überprüfung auszuführen.<br/>    |



 

 


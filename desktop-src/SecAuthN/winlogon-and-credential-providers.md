---
description: Ist das Windows-Modul, das die interaktive Anmeldung für eine Anmelde Sitzung ausführt. Das Winlogon-Verhalten kann durch Implementieren und Registrieren eines Anmelde Informationsanbieters angepasst werden.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon-und Anmelde Informationsanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958869"
---
# <a name="winlogon-and-credential-providers"></a>Winlogon-und Anmelde Informationsanbieter

[*Winlogon*](../secgloss/w-gly.md) ist das Windows-Modul, das die interaktive Anmeldung für eine [*Anmelde Sitzung*](../secgloss/l-gly.md)ausführt. Das Winlogon-Verhalten kann durch Implementieren und Registrieren eines Anmelde Informationsanbieters angepasst werden.

Weitere Informationen zum Implementieren eines Anmelde Informationsanbieters finden Sie in den folgenden Themen.



| Thema                                                                                                           | BESCHREIBUNG                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Vom Anmelde Informationsanbieter gesteuerte Windows-Anmeldevorgang](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | Übersicht über die Winlogon-und Anmelde Informationsanbieter-Architektur und einen Beispiel-Anmelde Informationsanbieter.<br/> |
| [Shellschnittstellen](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | Referenz zur Anmelde Informationsanbieter-Schnittstelle.<br/>                                                    |
| [Anmelde Informationsanbieter in Windows 10](credential-providers-in-windows.md)<br/>                            | Drittanbieter-Anmelde Informationsanbieter und System Anmelde Informationsanbieter in Windows 10.<br/>             |



 

Eine Beispiel Implementierung für den Anmelde Informationsanbieter finden Sie im Beispiel im Windows SDK-Installationsverzeichnis unter \\ Samples \\ Security \\ kredentialprovider.

**Windows Server 2003 und Windows XP:** Anmelde Informationsanbieter werden nicht unterstützt. Weitere Informationen zum Anpassen von Winlogon finden Sie unter [Winlogon und Gina](winlogon-and-gina.md).

 

 

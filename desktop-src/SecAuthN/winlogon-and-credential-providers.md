---
description: Das Windows Modul, das die interaktive Anmeldung für eine Anmeldesitzung ausführt. Das Winlogon-Verhalten kann angepasst werden, indem ein Anmeldeinformationsanbieter implementiert und registriert wird.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon- und Anmeldeinformationsanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a110c741289de9fdd08f1f5d5c820e9695f057b1d74db2e56f014f5da28eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785770"
---
# <a name="winlogon-and-credential-providers"></a>Winlogon- und Anmeldeinformationsanbieter

[*Winlogon*](../secgloss/w-gly.md) ist das Windows Modul, das die interaktive Anmeldung für eine [*Anmeldesitzung*](../secgloss/l-gly.md)ausführt. Das Winlogon-Verhalten kann angepasst werden, indem ein Anmeldeinformationsanbieter implementiert und registriert wird.

Informationen zum Implementieren eines Anmeldeinformationsanbieter finden Sie in den folgenden Themen.



| Thema                                                                                                           | BESCHREIBUNG                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Anmeldeinformationsanbieter-gesteuerte Windows-Anmeldung](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | Übersicht über die Winlogon- und Anmeldeinformationsanbieter-Architektur und eine Beispiel-Anmeldeinformationsanbieter.<br/> |
| [Shellschnittstellen](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | Anmeldeinformationsanbieter Schnittstellenreferenz.<br/>                                                    |
| [Anmeldeinformationsanbieter in Windows 10](credential-providers-in-windows.md)<br/>                            | Anbieter von Anmeldeinformationen von Drittanbietern und Anbieter von Systemanmeldeinformationen in Windows 10.<br/>             |



 

Ein Beispiel Anmeldeinformationsanbieter Implementierung finden Sie im Beispiel im Installationsverzeichnis des Windows SDK unter \\ Samples \\ Security \\ CredentialProvider.

**Windows Server 2003 und Windows XP:** Anmeldeinformationsanbieter werden nicht unterstützt. Informationen zum Anpassen von Winlogon finden Sie unter [Winlogon und GINA.](winlogon-and-gina.md)

 

 

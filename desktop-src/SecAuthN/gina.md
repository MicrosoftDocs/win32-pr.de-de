---
description: Der Zweck einer Gina-DLL besteht darin, anpassbare benutzeridentifizierungs-und Authentifizierungsverfahren bereitzustellen. Die Standard-Gina übernimmt dies durch Delegieren der SAS-Ereignisüberwachung an Winlogon, das CTL + ALT + ENTF-Taste (Secure Monitoring Sequenzen, SASs) empfängt und verarbeitet.
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: Gina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758268"
---
# <a name="gina"></a>Gina

Die [*Gina*](/windows/desktop/SecGloss/g-gly) arbeitet im [*Kontext*](/windows/desktop/SecGloss/c-gly) des [*Winlogon*](/windows/desktop/SecGloss/w-gly) -Prozesses, sodass die Gina-DLL sehr früh im Startvorgang geladen wird. Die Gina-DLL muss Regeln befolgen, damit die Integrität des Systems beibehalten wird, insbesondere in Bezug auf die Interaktion mit dem Benutzer.

> [!Note]  
> Gina-DLLs werden in Windows Vista ignoriert.

 

Die Gina wird häufig verwendet, um mit einem externen Gerät wie z. b. einem [*Smartcardleser*](/windows/desktop/SecGloss/r-gly)zu kommunizieren. Es ist von entscheidender Bedeutung, den Startparameter für den Gerätetreiber auf System (WinNT. h: Service \_ System \_ Start) festzulegen, um sicherzustellen, dass der Treiber zum Zeitpunkt des aufgerufenen von Gina geladen wird.

Der Zweck einer Gina-DLL besteht darin, anpassbare benutzeridentifizierungs-und Authentifizierungsverfahren bereitzustellen. Die Standard-Gina übernimmt dies durch Delegieren der SAS-Ereignisüberwachung an Winlogon, das CTL + ALT + ENTF-Taste ( [*Secure Monitoring Sequenzen*](/windows/desktop/SecGloss/s-gly) , SASs) empfängt und verarbeitet. Eine benutzerdefinierte Gina ist dafür verantwortlich, sich selbst für das Empfangen von SAS-Ereignissen (außer der standardmäßigen Taste STRG + ALT + ENTF) und die Benachrichtigung von Winlogon, wenn SAS-Ereignisse auftreten, einzurichten. Winlogon wertet seinen Status aus, um zu bestimmen, was für die Verarbeitung der benutzerdefinierten Gina-SAS erforderlich ist. Diese Verarbeitung beinhaltet in der Regel Aufrufe der SAS-Verarbeitungsfunktionen von Gina.

Informationen zu bestimmten Gina-Exportfunktionen finden Sie unter [Gina-Exportfunktionen](authentication-functions.md). Informationen zum Verwenden von Gina-Strukturen zum Übergeben von Informationen finden Sie unter [Gina-Strukturen](authentication-structures.md).



| Thema                                                                             | BESCHREIBUNG                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Laden und Ausführen einer Gina-dll](loading-and-running-a-gina-dll.md)<br/>   | Welcher Registrierungsschlüssel Wert geändert wird, um eine benutzerdefinierte GINA-DLL zu laden und auszuführen.<br/> |
| [Entwickeln und Testen einer Gina-dll](building-and-testing-a-gina-dll.md)<br/> | So testen Sie eine Gina-DLL.<br/>                                              |



 

 


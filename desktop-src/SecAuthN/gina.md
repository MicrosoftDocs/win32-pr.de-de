---
description: Der Zweck einer GINA-DLL besteht darin, anpassbare Benutzeridentifikations- und Authentifizierungsverfahren bereitzustellen. Die Standard-GINA delegiert die SAS-Ereignisüberwachung an Winlogon, das CTL+ALT+DEL Secure Attention Sequences (SASs) empfängt und verarbeitet.
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: Gina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dad8917a24100fbf5c6c36eab3bbfc5b67baf62b378f9207626378fe864b672
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623140"
---
# <a name="gina"></a>Gina

Die [*GINA*](/windows/desktop/SecGloss/g-gly) wird im [*Kontext*](/windows/desktop/SecGloss/c-gly) des [*Winlogon-Prozesses*](/windows/desktop/SecGloss/w-gly) betrieben, und daher wird die GINA-DLL sehr früh im Startprozess geladen. Die GINA-DLL muss Regeln befolgen, damit die Integrität des Systems erhalten bleibt, insbesondere in Bezug auf die Interaktion mit dem Benutzer.

> [!Note]  
> GINA-DLLs werden in Windows Vista ignoriert.

 

Die gängigste Verwendung der GINA ist die Kommunikation mit einem externen Gerät, z. B. einem [*Smartcardleser.*](/windows/desktop/SecGloss/r-gly) Es ist wichtig, den Startparameter für den Gerätetreiber auf system (Winnt.h: SERVICE \_ SYSTEM \_ START) festzulegen, um sicherzustellen, dass der Treiber zum Zeitpunkt des Aufrufs der GINA geladen wird.

Der Zweck einer GINA-DLL besteht darin, anpassbare Benutzeridentifikations- und Authentifizierungsverfahren bereitzustellen. Die Standard-GINA delegiert die SAS-Ereignisüberwachung an Winlogon, das CTL+ALT+DEL [*Secure Attention Sequences*](/windows/desktop/SecGloss/s-gly) (SASs) empfängt und verarbeitet. Eine benutzerdefinierte GINA ist dafür verantwortlich, sich so einzurichten, dass SAS-Ereignisse empfangen werden (mit Ausnahme des Standardereignisses STRG+ALT+DEL SAS) und Winlogon benachrichtigt wird, wenn SAS-Ereignisse auftreten. Winlogon wertet seinen Zustand aus, um zu bestimmen, was erforderlich ist, um die SAS der benutzerdefinierten GINA zu verarbeiten. Diese Verarbeitung umfasst in der Regel Aufrufe der SAS-Verarbeitungsfunktionen der GINA.

Informationen zu bestimmten GINA-Exportfunktionen finden Sie unter [GINA-Exportfunktionen.](authentication-functions.md) Informationen zur Verwendung von GINA-Strukturen zum Übergeben von Informationen finden Sie unter [GINA-Strukturen.](authentication-structures.md)



| Thema                                                                             | Beschreibung                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Laden und Ausführen einer GINA-DLL](loading-and-running-a-gina-dll.md)<br/>   | Welcher Registrierungsschlüsselwert geändert werden soll, um eine benutzerdefinierte GINA-DLL zu laden und auszuführen.<br/> |
| [Erstellen und Testen einer GINA-DLL](building-and-testing-a-gina-dll.md)<br/> | Testen einer GINA-DLL<br/>                                              |



 

 


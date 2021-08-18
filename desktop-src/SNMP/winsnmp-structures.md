---
title: WinSNMP-Strukturen
description: Die WinSNMP-API-Funktionen verwenden die folgenden Strukturen.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- WinSNMP-Strukturen SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b409b6d12063ebd3feb9c663f2d607bc5ceead0462b2945334f1e7e691c9be63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142753"
---
# <a name="winsnmp-structures"></a>WinSNMP-Strukturen

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-Man handelt.\]

Die WinSNMP-API-Funktionen verwenden die folgenden Strukturen.



| Struktur                                  | Beschreibung                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | Enthält einen 64-Bit-Ganzzahlwert ohne Vorzeichen, der einen Zähler darstellt.                                                    |
| [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | Enthält einen Zeiger auf eine SNMP-Oktettzeichenfolge variabler Länge.                                                         |
| [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | Enthält einen Zeiger auf ein Array variabler Länge der Unteridentitäten, die einem angegebenen benannten Objekt zugeordnet sind. |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | Stellt den Wert dar, der einem Variablennamen in einem Variablenbindungseintrag zugeordnet ist.                              |
| [**smiVENDORINFO**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | Enthält Informationen zur Microsoft-Implementierung von WinSNMP.                                                    |



 

 

 
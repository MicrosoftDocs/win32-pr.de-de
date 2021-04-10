---
title: WinSNMP-Strukturen
description: Die WinSNMP-API-Funktionen verwenden die folgenden Strukturen.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- WinSNMP-Strukturen SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858352"
---
# <a name="winsnmp-structures"></a>WinSNMP-Strukturen

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Die WinSNMP-API-Funktionen verwenden die folgenden Strukturen.



| Struktur                                  | BESCHREIBUNG                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | Enthält einen 64-Bit-Ganzzahl-Wert ohne Vorzeichen, der einen Leistungs Bezeichner darstellt.                                                    |
| [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | Enthält einen Zeiger auf eine SNMP-Oktett-Zeichenfolge variabler Länge.                                                         |
| [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | Enthält einen Zeiger auf ein Array variabler Länge der unter Elemente, die einem angegebenen benannten Objekt zugeordnet sind. |
| [**smivalue**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | Stellt den Wert dar, der einem Variablennamen in einem Variablen Bindungs Eintrag zugeordnet ist.                              |
| [**smivendorinfo**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | Enthält Informationen über die Microsoft-Implementierung von winsnmp.                                                    |



 

 

 
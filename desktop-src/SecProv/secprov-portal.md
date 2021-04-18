---
description: Die WMI-Sicherheitsanbieter können für die WMI-Skripterstellung und für die Erstellung eines verwalteten Sicherheits Anbieters verwendet werden.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: WMI-Anbieter für Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0206e337e5fa23470f015a0264bd77d53e8c4e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354449"
---
# <a name="security-wmi-providers"></a>WMI-Anbieter für Sicherheit

## <a name="purpose"></a>Zweck

Die WMI-Anbieter für Sicherheit ermöglichen es Administratoren und Programmierern, BitLocker-Laufwerkverschlüsselung (BDE) und Trusted Platform Module (TPM) mithilfe von Windows-Verwaltungsinstrumentation (WMI) zu konfigurieren.

## <a name="developer-audience"></a>Entwicklergruppe

In diesem Dokument wird die WMI-Anbieter Schnittstelle zum Verwalten und Konfigurieren von BitLocker-Laufwerkverschlüsselung (BDE) und Trusted Platform Module (TPM) auf Windows Server 2008 R2 und Windows Server 2008 für-Server sowie Windows 7 und Windows Vista für Client Computer angegeben. Sie soll von denjenigen gelesen werden, die Skripts, Benutzeroberflächen Elemente oder andere Verwaltungs Tools für BDE oder das TPM schreiben.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die WMI-Sicherheitsanbieter benötigen die MOF-Datei, die mit den einzelnen Anbietern und einem unterstützten Betriebssystem angegeben wird. Das mindestbetriebssystem ist entweder Windows Server 2008 oder Windows Vista. BitLocker-Laufwerkverschlüsselung ist nur für die Windows Vista Enterprise-und Windows Vista Ultimate-Versionen von Windows Vista verfügbar. Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                               | BESCHREIBUNG                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Informationen zu WMI-Sicherheitsanbietern](about-security-wmi-providers.md)<br/>         | Kurze Übersicht über die WMI-Sicherheitsanbieter.<br/>           |
| [WMI-Anbieter Referenz für Sicherheit](security-wmi-providers-reference.md)<br/> | Referenz Dokumentation für die WMI-Sicherheitsanbieter.<br/> |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Im folgenden finden Sie weitere Ressourcen.



|                    |                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Klassen<br/> | Weitere Informationen zu den WMI-Sicherheitsanbietern finden Sie unter [**Win32 \_ verschlüsseltablevolume**](win32-encryptablevolume.md) und [**Win32 \_ TPM**](win32-tpm.md).<br/> |



 

 

 





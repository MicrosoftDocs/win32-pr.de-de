---
description: Die WMI-Sicherheitsanbieter können für wmi-Skripts und zum Erstellen eines verwalteten Sicherheitsanbieters verwendet werden.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: WMI-Sicherheitsanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acc0ecff578f687b7a0473fc5ecbbeae6b3a5503deb795da3bddfe6bf761042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080620"
---
# <a name="security-wmi-providers"></a>WMI-Sicherheitsanbieter

## <a name="purpose"></a>Zweck

Die WMI-Sicherheitsanbieter ermöglichen Es Administratoren und Programmierern, BitLocker-Laufwerkverschlüsselung (BDE) und die Trusted Platform Module (TPM) mithilfe der Windows Management Instrumentation (WMI) zu konfigurieren.

## <a name="developer-audience"></a>Entwicklergruppe

Dieses Dokument gibt die WMI-Anbieterschnittstelle zum Verwalten und Konfigurieren von BitLocker-Laufwerkverschlüsselung (BDE) und Trusted Platform Module (TPM) auf Windows Server 2008 R2 und Windows Server 2008 für Server sowie Windows 7 und Windows Vista für Clientcomputer an. Sie soll von Benutzern gelesen werden, die Skripts, Benutzeroberflächenelemente oder andere Verwaltungstools für BDE oder tpm schreiben.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die WMI-Sicherheitsanbieter erfordern die MOF-Datei, die mit jedem Anbieter und einem unterstützten Betriebssystem angegeben ist. Das Mindestbetriebssystem ist entweder Windows Server 2008 oder Windows Vista. BitLocker-Laufwerkverschlüsselung ist nur für die versionen Windows Vista Enterprise und Windows Vista Ultimate von Windows Vista verfügbar. Informationen zu Laufzeitanforderungen für ein bestimmtes Programmierelement finden Sie im Abschnitt Anforderungen der Referenzseite für dieses Element.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                               | BESCHREIBUNG                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Informationen zu WMI-Sicherheitsanbietern](about-security-wmi-providers.md)<br/>         | Kurze Übersicht über die Sicherheits-WMI-Anbieter.<br/>           |
| [WMI-Anbieterreferenz für die Sicherheit](security-wmi-providers-reference.md)<br/> | Referenzdokumentation für die Sicherheits-WMI-Anbieter.<br/> |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Im Folgenden finden Sie zusätzliche Ressourcen.



| Ressource     | BESCHREIBUNG                                                                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Klassen      | Weitere Informationen zu den WMI-Sicherheitsanbietern finden Sie unter [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) und [**Win32 \_ Tpm.**](win32-tpm.md) |



 

 

 





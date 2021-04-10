---
description: Der Schannel SSP implementiert Versionen der TLS-, DTLS-und SSL-Protokolle. Unterschiedliche Windows-Versionen unterstützen verschiedene Protokoll Versionen.
ms.assetid: FF716A4E-ABF2-4773-9588-9D200945A866
title: Protokolle in TLS/SSL (Schannel SSP)
ms.topic: article
ms.date: 01/20/2021
ms.custom: contperf-fy21q3
ms.openlocfilehash: 844d75230119b747f77697f67ddecec5f64ce7cf
ms.sourcegitcommit: 07b756a2f350efa5cfd5024a723ef392274ac3d9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "103961090"
---
# <a name="protocols-in-tlsssl-schannel-ssp"></a>Protokolle in TLS/SSL (Schannel SSP)

Der Schannel SSP implementiert Versionen der TLS-, DTLS-und SSL-Protokolle. Unterschiedliche Windows-Versionen unterstützen verschiedene Protokoll Versionen.

## <a name="tls-protocol-version-support"></a>Unterstützung für TLS-Protokoll Versionen

In der folgenden Tabelle wird die Unterstützung für TLS-Protokoll Versionen des Microsoft SChannel-Anbieters angezeigt.

*Tipp: Sie müssen möglicherweise horizontal einen Bildlauf durchführen, um alle Spalten in dieser Tabelle anzuzeigen:*

| Windows-Betriebssystem | TLS 1,0-Client | TLS 1,0-Server | TLS 1,1-Client | TLS 1,1-Server | TLS 1,2-Client | TLS 1,2-Server | TLS 1,3-Client | TLS 1,3-Server |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Windows Vista/Windows Server 2008                     | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  | Nicht unterstützt  | Nicht unterstützt  | Nicht unterstützt  | Nicht unterstützt  |
| Windows Server 2008 mit Service Pack 2 (SP2)         | Aktiviert        | Aktiviert        | Disabled       | Disabled       | Disabled       | Disabled       | Nicht unterstützt  | Nicht unterstützt  |
| Windows 7/Windows Server 2008 R2                      | Aktiviert        | Aktiviert        | Disabled       | Disabled       | Disabled       | Disabled       | Nicht unterstützt  | Nicht unterstützt  |
| Windows 8/Windows Server 2012                         | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 8.1/Windows Server 2012 R2                    | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1507                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1511                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1607/Windows Server 2016 Standard | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1703                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1709                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1803                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1809                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1903                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1909                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  | 
| Windows 10, Version 2004                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 20H2                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows Server 2022                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        |


## <a name="dtls-protocol-version-support"></a>Unterstützung der DTLS-Protokollversion

Im folgenden wird die Unterstützung von DTLS-Protokoll Versionen durch den Microsoft SChannel-Anbieter aufgelistet.

*Tipp: Sie müssen möglicherweise horizontal einen Bildlauf durchführen, um alle Spalten in dieser Tabelle anzuzeigen:*

| Windows-Betriebssystem                                            | DTLS 1,0-Client | DTLS 1,0-Server | DTLS 1,2-Client | DTLS 1,2-Server |
|-------------------------------------------------------|-----------------|-----------------|-----------------|-----------------|
| Windows Vista/Windows Server 2008                     | Nicht unterstützt   | Nicht unterstützt   | Nicht unterstützt   | Nicht unterstützt   |
| Windows Server 2008 mit SP2                          | Nicht unterstützt   | Nicht unterstützt   | Nicht unterstützt   | Nicht unterstützt   |
| Windows 7/Windows Server 2008 R2                      | Aktiviert         | Aktiviert         | Nicht unterstützt   | Nicht unterstützt   |
| Windows 8/Windows Server 2012                         | Aktiviert         | Aktiviert         | Nicht unterstützt   | Nicht unterstützt   |
| Windows 8.1/Windows Server 2012 R2                    | Aktiviert         | Aktiviert         | Nicht unterstützt   | Nicht unterstützt   |
| Windows 10, Version 1507                              | Aktiviert         | Aktiviert         | Nicht unterstützt   | Nicht unterstützt   |
| Windows 10, Version 1511                              | Aktiviert         | Aktiviert         | Nicht unterstützt   | Nicht unterstützt   |
| Windows 10, Version 1607/Windows Server 2016 Standard | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 1703                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 1803                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 1809                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 1903                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 1909                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 2004                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 20H2                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 21h1                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |

## <a name="pre-tls-standard-protocols-support"></a>Unterstützung von Standardprotokollen für Pre-TLS

Im folgenden finden Sie eine Liste der Microsoft SChannel-Anbieter Unterstützung für Standardprotokolle von Standard-TLS:

*Tipp: Sie müssen möglicherweise horizontal einen Bildlauf durchführen, um alle Spalten in dieser Tabelle anzuzeigen:*

| Windows-Betriebssystem                                            | PCT 1.0       | SSL2 verwendet-Client   | SSL2 verwendet-Server   | SSL3-Client | SSL3-Server |
|-------------------------------------------------------|---------------|---------------|---------------|-------------|-------------|
| Windows Vista/Windows Server 2008                     | Nicht unterstützt | Disabled      | Aktiviert       | Aktiviert     | Aktiviert     |
| Windows Server 2008 mit SP2                          | Nicht unterstützt | Disabled      | Aktiviert       | Aktiviert     | Aktiviert     |
| Windows 7/Windows Server 2008 R2                      | Nicht unterstützt | Disabled      | Aktiviert       | Aktiviert     | Aktiviert     |
| Windows 8/Windows Server 2012                         | Nicht unterstützt | Disabled      | Disabled      | Aktiviert     | Aktiviert     |
| Windows 8.1/Windows Server 2012 R2                    | Nicht unterstützt | Disabled      | Disabled      | Aktiviert     | Aktiviert     |
| Windows 10, Version 1507                              | Nicht unterstützt | Disabled      | Disabled      | Aktiviert     | Aktiviert     |
| Windows 10, Version 1511                              | Nicht unterstützt | Disabled      | Disabled      | Aktiviert     | Aktiviert     |
| Windows 10, Version 1607/Windows Server 2016 Standard | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 1703                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 1803                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 1809                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 1903                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 1909                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 2004                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 20H2                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 20h1                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |


> [!IMPORTANT]
> Ab Windows 10, Version 1607 und Windows Server 2016, wurde SSL 2,0 entfernt und wird nicht mehr unterstützt.

> [!TIP]  
> Alle Versionen von Windows akzeptieren eine einheitliche Format Meldung "ClientHello", auch wenn SSL Version 2 deaktiviert oder nicht mehr unterstützt wird.

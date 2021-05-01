---
description: Der Schannel-SSP implementiert Versionen der PROTOKOLLE TLS, DTLS und SSL. Verschiedene Windows-Versionen unterstützen verschiedene Protokollversionen.
ms.assetid: FF716A4E-ABF2-4773-9588-9D200945A866
title: Protokolle in TLS/SSL (Schannel SSP)
ms.topic: article
ms.date: 01/20/2021
ms.custom: contperf-fy21q3
ms.openlocfilehash: 4717a128602d2ae52f90e6e201c6f6ff6aeb1de2
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332415"
---
# <a name="protocols-in-tlsssl-schannel-ssp"></a>Protokolle in TLS/SSL (Schannel SSP)

Der Schannel-SSP implementiert Versionen der PROTOKOLLE TLS, DTLS und SSL. Verschiedene Windows-Versionen unterstützen verschiedene Protokollversionen.

## <a name="tls-protocol-version-support"></a>Unterstützung der TLS-Protokollversion

In der folgenden Tabelle wird die Unterstützung von TLS-Protokollversionen durch den Microsoft Schannel-Anbieter angezeigt.

*Tipp: Möglicherweise müssen Sie horizontal scrollen, um alle Spalten in dieser Tabelle anzuzeigen:*

| Windows-Betriebssystem | TLS 1.0-Client | TLS 1.0-Server | TLS 1.1-Client | TLS 1.1-Server | TLS 1.2-Client | TLS 1.2-Server | TLS 1.3-Client | TLS 1.3-Server |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Windows Vista/Windows Server 2008                     | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  | Nicht unterstützt  | Nicht unterstützt  | Nicht unterstützt  | Nicht unterstützt  |
| Windows Server 2008 mit Service Pack 2 (SP2)         | Aktiviert        | Aktiviert        | Disabled       | Disabled       | Disabled       | Disabled       | Nicht unterstützt  | Nicht unterstützt  |
| Windows 7/Windows Server 2008 R2                      | Aktiviert        | Aktiviert        | Disabled       | Disabled       | Disabled       | Disabled       | Nicht unterstützt  | Nicht unterstützt  |
| Windows 8/Windows Server 2012                         | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 8.1/Windows Server 2012 R2                    | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1507                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1511                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, version 1607/Windows Server 2016 Standard | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1703                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1709                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1803                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1809/Windows Server 2019                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1903                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 1909                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  | 
| Windows 10, Version 2004                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows 10, Version 20H2                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Nicht unterstützt  | Nicht unterstützt  |
| Windows Server 2022                              | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        | Aktiviert        |


## <a name="dtls-protocol-version-support"></a>Unterstützung der DTLS-Protokollversion

Im Folgenden wird die Unterstützung von DTLS-Protokollversionen durch den Microsoft Schannel-Anbieter aufgeführt.

*Tipp: Möglicherweise müssen Sie horizontal scrollen, um alle Spalten in dieser Tabelle anzeigen zu können:*

| Windows-Betriebssystem                                            | DTLS 1.0-Client | DTLS 1.0-Server | DTLS 1.2-Client | DTLS 1.2-Server |
|-------------------------------------------------------|-----------------|-----------------|-----------------|-----------------|
| Windows Vista/Windows Server 2008                     | Nicht unterstützt   | Nicht unterstützt   | Nicht unterstützt   | Nicht unterstützt   |
| Windows Server 2008 mit SP2                          | Nicht unterstützt   | Nicht unterstützt   | Nicht unterstützt   | Nicht unterstützt   |
| Windows 7/Windows Server 2008 R2                      | Aktiviert         | Aktiviert         | Nicht unterstützt   | Nicht unterstützt   |
| Windows 8/Windows Server 2012                         | Aktiviert         | Aktiviert         | Nicht unterstützt   | Nicht unterstützt   |
| Windows 8.1/Windows Server 2012 R2                    | Aktiviert         | Aktiviert         | Nicht unterstützt   | Nicht unterstützt   |
| Windows 10, Version 1507                              | Aktiviert         | Aktiviert         | Nicht unterstützt   | Nicht unterstützt   |
| Windows 10, Version 1511                              | Aktiviert         | Aktiviert         | Nicht unterstützt   | Nicht unterstützt   |
| Windows 10, version 1607/Windows Server 2016 Standard | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 1703                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 1803                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 1809                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 1903                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 1909                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 2004                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 20H2                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |
| Windows 10, Version 21H1                              | Aktiviert         | Aktiviert         | Aktiviert         | Aktiviert         |

## <a name="pre-tls-standard-protocols-support"></a>Unterstützung von Standardprotokollen vor TLS

Im Folgenden wird die Unterstützung von Vor-TLS-Standardprotokollen durch den Microsoft Schannel-Anbieter aufgeführt:

*Tipp: Möglicherweise müssen Sie horizontal scrollen, um alle Spalten in dieser Tabelle anzeigen zu können:*

| Windows-Betriebssystem                                            | PCT 1.0       | SSL2-Client   | SSL2-Server   | SSL3-Client | SSL3-Server |
|-------------------------------------------------------|---------------|---------------|---------------|-------------|-------------|
| Windows Vista/Windows Server 2008                     | Nicht unterstützt | Disabled      | Aktiviert       | Aktiviert     | Aktiviert     |
| Windows Server 2008 mit SP2                          | Nicht unterstützt | Disabled      | Aktiviert       | Aktiviert     | Aktiviert     |
| Windows 7/Windows Server 2008 R2                      | Nicht unterstützt | Disabled      | Aktiviert       | Aktiviert     | Aktiviert     |
| Windows 8/Windows Server 2012                         | Nicht unterstützt | Disabled      | Disabled      | Aktiviert     | Aktiviert     |
| Windows 8.1/Windows Server 2012 R2                    | Nicht unterstützt | Disabled      | Disabled      | Aktiviert     | Aktiviert     |
| Windows 10, Version 1507                              | Nicht unterstützt | Disabled      | Disabled      | Aktiviert     | Aktiviert     |
| Windows 10, Version 1511                              | Nicht unterstützt | Disabled      | Disabled      | Aktiviert     | Aktiviert     |
| Windows 10, version 1607/Windows Server 2016 Standard | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 1703                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 1803                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 1809                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 1903                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 1909                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 2004                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 20H2                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |
| Windows 10, Version 20H1                              | Nicht unterstützt | Nicht unterstützt | Nicht unterstützt | Disabled    | Disabled    |


> [!IMPORTANT]
> Ab Windows 10 Version 1607 und Windows Server 2016 wurde SSL 2.0 entfernt und wird nicht mehr unterstützt.

> [!TIP]  
> Alle Versionen von Windows akzeptieren die Meldung "ClientHello" im einheitlichen Format, auch wenn SSL-Version 2 deaktiviert oder nicht mehr unterstützt wird.

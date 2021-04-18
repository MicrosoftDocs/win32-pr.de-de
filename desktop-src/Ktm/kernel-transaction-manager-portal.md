---
description: Implementieren Sie Transaktions-NTFS (TxF) und Transaktions Registrierung (TxR). TxF ermöglicht Transaktions Dateisystem Vorgänge innerhalb von NTFS. TxR ermöglicht transaktive Registrierungs Vorgänge. Koordinieren Sie Dateisystem-und Registrierungs Vorgänge mit einer Transaktion.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Kerneltransaktions-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281050461163d5fd0cde64af79e70569d613888e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352509"
---
# <a name="kernel-transaction-manager"></a>Kerneltransaktions-Manager

## <a name="purpose"></a>Zweck

Der Kerneltransaktions-Manager (KTM) ermöglicht die Entwicklung von Anwendungen, die Transaktionen verwenden. Die Transaktions-Engine selbst befindet sich innerhalb des Kernels, Transaktionen können jedoch für Kernel-oder benutzermodustransaktionen und innerhalb eines einzelnen Hosts oder verteilter Hosts entwickelt werden.

Der KTM wird zum Implementieren von transaktionalen NTFS (TxF) und Transaktions Registrierung (TxR) verwendet. TxF ermöglicht Transaktions Dateisystem Vorgänge innerhalb des NTFS-Dateisystems. TxR ermöglicht transaktive Registrierungs Vorgänge. KTM ermöglicht Client Anwendungen das Koordinieren von Dateisystem-und Registrierungs Vorgängen mit einer Transaktion.

Zum Entwickeln einer Anwendung, die Transaktionen mit anderen Ressourcen als TxF oder TxR koordiniert, müssen Sie zunächst einen Dienst für die Win32-Transaktion entwickeln, der auch als Ressourcen-Manager bezeichnet wird.

Verwaltete und com+-Anwendungen sollten ihre nativen Transaktions-Manager verwenden.

## <a name="where-applicable"></a>Anwendungsbereich

KTM kann mit Anwendungen und Ressourcen-Managern verwendet werden, die unter Windows Vista oder Windows Server 2008 gehostet werden.

## <a name="developer-audience"></a>Entwicklergruppe

Die KTM-API ist für die Verwendung durch C-und C++-Programmierer konzipiert.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

KTM wird ab Windows Vista unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                     | BESCHREIBUNG                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Info](about-ktm.md)<br/>         | Allgemeine Informationen zu Transaktionen und den von KTM bereitgestellten Funktionen.<br/>                           |
| [Verweis](ktm-reference.md)<br/> | Dokumentation für die Funktionen, Datenstrukturen, Enumerationen und andere Programmier Elemente von KTM.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gemeinsames Protokolldateisystem](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[Transaktionale NTFS (TxF)](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> </dl>

 


---
description: Implementieren Sie Transactional NTFS (TxF) und Transactional Registry (TxR). TxF ermöglicht transaktive Dateisystemvorgänge in NTFS. TxR ermöglicht transaktive Registrierungsvorgänge. Koordinieren Sie Dateisystem- und Registrierungsvorgänge mit einer Transaktion.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Kerneltransaktions-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c446931fff4f119217a5f6e5f1b7ae8cf351cf94966a9da5abc4e4d2e88d787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897530"
---
# <a name="kernel-transaction-manager"></a>Kerneltransaktions-Manager

## <a name="purpose"></a>Zweck

Der KernelTransaktions-Manager (KTM) ermöglicht die Entwicklung von Anwendungen, die Transaktionen verwenden. Die Transaktions-Engine selbst befindet sich innerhalb des Kernels, aber Transaktionen können für Kernel- oder Benutzermodustransaktionen und innerhalb eines einzelnen Hosts oder zwischen verteilten Hosts entwickelt werden.

KTM wird verwendet, um Transaktions-NTFS (TxF) und Transaktionsregistrierung (Transactional Registry, TxR) zu implementieren. TxF ermöglicht transaktive Dateisystemvorgänge innerhalb des NTFS-Dateisystems. TxR ermöglicht transaktive Registrierungsvorgänge. Mit KTM können Clientanwendungen Dateisystem- und Registrierungsvorgänge mit einer Transaktion koordinieren.

Um eine Anwendung zu entwickeln, die Transaktionen mit anderen Ressourcen als TxF oder TxR koordiniert, müssen Sie zunächst einen Win32-transaktionsorientierten Dienst entwickeln, der auch als Ressourcen-Manager bezeichnet wird.

Verwaltete und COM+-Anwendungen sollten ihre nativen Transaktions-Manager verwenden.

## <a name="where-applicable"></a>Anwendungsbereich

KTM kann mit Anwendungen und Ressourcen-Managern verwendet werden, die auf Windows Vista oder Windows Server 2008 gehostet werden.

## <a name="developer-audience"></a>Entwicklergruppe

Die KTM-API ist für die Verwendung durch C- und C++-Programmierer konzipiert.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

KTM wird ab Windows Vista unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                     | Beschreibung                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Info](about-ktm.md)<br/>         | Allgemeine Informationen zu Transaktionen und den von KTM bereitgestellten Funktionen.<br/>                           |
| [Referenz](ktm-reference.md)<br/> | Dokumentation für die Funktionen, Datenstrukturen, Enumerationen und andere Programmierelemente von KTM.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gemeinsames Protokolldateisystem](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[Transaktionales NTFS (TxF)](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> </dl>

 


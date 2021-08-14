---
description: Transaktionales NTFS (TxF) ermöglicht das Durchführen von Dateivorgängen auf einem NTFS-Dateisystemvolume in einer Transaktion.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: Transaktionales NTFS (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5b44a35e4f83c1389d1fc2e6bc3de4f97f5ad203bbdee4750c2fcd26d87f47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431910"
---
# <a name="transactional-ntfs-txf"></a>Transaktionales NTFS (TxF)

\[Microsoft empfiehlt Entwicklern dringend, alternative Mittel zu verwenden, um die Anforderungen Ihrer Anwendung zu erfüllen. Viele Szenarien, für die TxF entwickelt wurde, können durch einfachere und leichter verfügbare Techniken erreicht werden. Darüber hinaus ist TxF in zukünftigen Versionen von Microsoft Windows möglicherweise nicht verfügbar. Weitere Informationen und Alternativen zu TxF finden Sie unter [Alternativen zur Verwendung von Transaktional NTFS](deprecation-of-txf.md).\]

## <a name="purpose"></a>Zweck

Transaktionales NTFS (TxF) ermöglicht das Durchführen von Dateivorgängen auf einem NTFS-Dateisystemvolume in einer Transaktion. TxF-Transaktionen erhöhen die Anwendungszuverlässigkeit, indem sie die Datenintegrität über Fehler hinweg schützen und die Anwendungsentwicklung vereinfachen, indem die Menge an Fehlerbehandlungscode erheblich reduziert wird.

TxF verwendet das Transaktionsframework, das vom [Kerneltransaktions-Manager (KERNEL Transaction Manager,](/windows/desktop/Ktm/kernel-transaction-manager-portal) WAD) bereitgestellt wird. Dadurch können TxF-Dateivorgänge Teil einer Transaktion sein, die andere Datenquellen wie SQL Server und Transacted Registry (TxR) umfasst.

## <a name="where-applicable"></a>Anwendungsbereich

Eine Anwendung kann TxF verwenden, um die Integrität von Daten auf dem Datenträger beizubehalten, die durch unerwartete Fehlerbedingungen verursacht werden, und gleichzeitige Dateisystembenutzerszenarios zu lösen, indem Sie Ihre Änderungen von anderen isolieren, während die Änderungen vorgenommen werden.

## <a name="developer-audience"></a>Entwicklergruppe

Vor der Verwendung von TxF sollten Sie über fundierte Kenntnisse zu Transaktionen mithilfe von ENTWEDER MIT oder [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85))verfügen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

TxF ist ab Windows Vista verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                    | Beschreibung                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Info](about-transactional-ntfs.md)<br/>         | Allgemeine Informationen zu Transaktions-NTFS.<br/>                                                   |
| [Referenz](transactional-ntfs-reference.md)<br/> | Dokumentation zu den Funktionen, Datenstrukturen, Enumerationen und anderen Programmierelementen.<br/> |



 

 


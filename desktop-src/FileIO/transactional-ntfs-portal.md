---
description: Transaktionale NTFS (TxF) ermöglicht die Ausführung von Datei Vorgängen auf einem NTFS-Dateisystem Volume in einer Transaktion.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: Transaktionale NTFS (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7553bfc7cae0b5389762527f0ac726c674a6a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524926"
---
# <a name="transactional-ntfs-txf"></a>Transaktionale NTFS (TxF)

\[Microsoft empfiehlt Entwicklern dringend, Alternative Möglichkeiten zum Erreichen der Anforderungen Ihrer Anwendung zu nutzen. Viele Szenarios, für die TxF entwickelt wurde, können mithilfe einfacherer und leichter verfügbarer Techniken erreicht werden. Außerdem ist TxF in zukünftigen Versionen von Microsoft Windows möglicherweise nicht verfügbar. Weitere Informationen und Alternativen zu TxF finden Sie unter [Alternativen zur Verwendung von transaktionalen NTFS](deprecation-of-txf.md).\]

## <a name="purpose"></a>Zweck

Transaktionale NTFS (TxF) ermöglicht die Ausführung von Datei Vorgängen auf einem NTFS-Dateisystem Volume in einer Transaktion. TxF-Transaktionen erhöhen die Anwendungs Zuverlässigkeit, indem Sie die Datenintegrität über Fehler hinweg schützen und die Anwendungsentwicklung vereinfachen, indem Sie den Code für die Fehlerbehandlung erheblich verringern.

TxF verwendet das Transaktions Framework, das vom [Kerneltransaktions-Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM) bereitgestellt wird. Dies ermöglicht die Ausführung von TxF-Datei Vorgängen in eine Transaktion mit anderen Datenquellen, z. b. SQL Server und Transaktions Registrierung (TxR).

## <a name="where-applicable"></a>Anwendungsbereich

Eine Anwendung kann TxF verwenden, um die Integrität der Daten auf dem Datenträger beizubehalten, die durch unerwartete Fehlerbedingungen verursacht werden, und unterstützt die Auflösung paralleler Dateisystem-Benutzer Szenarien, indem Ihre Änderungen von anderen isoliert werden, während die Änderungen vorgenommen werden.

## <a name="developer-audience"></a>Entwicklergruppe

Vor der Verwendung von TxF sollten Sie über ein funktionierendes wissen über Transaktionen verfügen, indem Sie entweder KTM oder [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85))verwenden.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

TxF ist ab Windows Vista verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                    | BESCHREIBUNG                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Info](about-transactional-ntfs.md)<br/>         | Allgemeine Informationen zu Transaktions-NTFS.<br/>                                                   |
| [Verweis](transactional-ntfs-reference.md)<br/> | Dokumentation für die Funktionen, Datenstrukturen, Enumerationen und andere Programmier Elemente.<br/> |



 

 


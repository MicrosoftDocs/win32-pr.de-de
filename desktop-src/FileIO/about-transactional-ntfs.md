---
description: Transaktionale NTFS (TxF) integriert Transaktionen in das NTFS-Dateisystem, wodurch Anwendungsentwicklern und Administratoren das ordnungsgemäße behandeln von Fehlern und das Beibehalten der Datenintegrität vereinfachen.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: Informationen zu Transaktions-NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343639"
---
# <a name="about-transactional-ntfs"></a>Informationen zu Transaktions-NTFS

\[Microsoft empfiehlt Entwicklern dringend, Alternative Möglichkeiten zum Erreichen der Anforderungen Ihrer Anwendung zu nutzen. Viele Szenarios, für die TxF entwickelt wurde, können mithilfe einfacherer und leichter verfügbarer Techniken erreicht werden. Außerdem ist TxF in zukünftigen Versionen von Microsoft Windows möglicherweise nicht verfügbar. Weitere Informationen und Alternativen zu TxF finden Sie unter [Alternativen zur Verwendung von transaktionalen NTFS](deprecation-of-txf.md).\]

Transaktionale NTFS (TxF) integriert Transaktionen in das NTFS-Dateisystem, wodurch Anwendungsentwicklern und Administratoren das ordnungsgemäße behandeln von Fehlern und das Beibehalten der Datenintegrität vereinfachen.

TxF kann an verteilten Transaktionen teilnehmen, die die [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) -Koordinaten enthalten, sodass Sie TxF für Folgendes verwenden können:

-   Transaktionen, die mehrere Datenspeicher umfassen, z. b. eine einzelne Transaktion für Datei-und SQL-Vorgänge
-   Transaktionen, die mehrere Computer umfassen, z. b. eine einzelne Transaktion für Datei Updates auf mehreren Computern

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                 | BESCHREIBUNG                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Verwendungszwecke von transaktionalen NTFS](when-to-use-transactional-ntfs.md)<br/>                                       | Verwenden Sie Transaktions-NTFS, um die Datenintegrität beizubehalten.<br/>                                                                        |
| [Bereitstellen von transaktionalen NTFS](deploying-transactional-ntfs.md)<br/>                                           | Caching-Steuerelement in transaktionalen NTFS.<br/>                                                                                    |
| [Verwenden von transaktionalen NTFS](how-to-use-transactional-ntfs.md)<br/>                                         | Verwalten von transaktiven Datei Handles in Transaktions-NTFS.<br/>                                                                   |
| [Grundlegende TxF-Konzepte](txf-basic-concepts.md)<br/>                                                               | Beschreibt die Konsistenz mit Lese-und Schreibzugriff, die Isolation mit Lese-und Schreibzugriff sowie die Konzepte von Transaktions Sperren in Transaktions-NTFS.<br/> |
| [Überlegungen zur Programmierung für transaktionale NTFS](programming-considerations-for-transacted-fileio-.md)<br/> | Beschreibt verschiedene Programmier Überlegungen für Transaktions-NTFS.<br/>                                                      |
| [Überlegungen zur Leistung von transaktionalen NTFS](performance-considerations-for-transactional-ntfs.md)<br/> | Empfehlungen für optimale Dateisystem Transaktionen.<br/>                                                                     |



 

 


---
description: Transaktionales NTFS (TxF) integriert Transaktionen in das NTFS-Dateisystem, wodurch Anwendungsentwickler und Administratoren die ordnungsgemäßen Fehler behandeln und die Datenintegrität beibehalten können.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: Informationen zu Transaktional NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404dc966673eac9d61229ab127877941fe82354ddffcfd021ba76b9931c8e097
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102110"
---
# <a name="about-transactional-ntfs"></a>Informationen zu Transaktional NTFS

\[Microsoft empfiehlt Entwicklern dringend, alternative Mittel zu verwenden, um die Anforderungen Ihrer Anwendung zu erfüllen. Viele Szenarien, für die TxF entwickelt wurde, können durch einfachere und leichter verfügbare Techniken erreicht werden. Darüber hinaus ist TxF in zukünftigen Versionen von Microsoft Windows möglicherweise nicht verfügbar. Weitere Informationen und Alternativen zu TxF finden Sie unter [Alternativen zur Verwendung von Transaktional NTFS](deprecation-of-txf.md).\]

Transaktionales NTFS (TxF) integriert Transaktionen in das NTFS-Dateisystem, wodurch Anwendungsentwickler und Administratoren die ordnungsgemäßen Fehler behandeln und die Datenintegrität beibehalten können.

TxF kann an verteilten Transaktionen teilnehmen, die von der [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) koordiniert werden, sodass Sie TxF für Folgendes verwenden können:

-   Transaktionen, die mehrere Datenspeicher umfassen, z. B. eine einzelne Transaktion für Datei- und SQL vorgänge
-   Transaktionen, die sich über mehrere Computer erstrecken, z. B. eine einzelne Transaktion für Dateiupdates auf mehreren Computern

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                 | BESCHREIBUNG                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Wann sollte ntfs für Transaktionen verwendet werden?](when-to-use-transactional-ntfs.md)<br/>                                       | Verwenden Sie transaktionales NTFS, um die Datenintegrität aufrechtzuerhalten.<br/>                                                                        |
| [Bereitstellen von transaktionalem NTFS](deploying-transactional-ntfs.md)<br/>                                           | Zwischenspeicherungssteuerelement in Transaktional NTFS.<br/>                                                                                    |
| [Verwenden von transaktionalem NTFS](how-to-use-transactional-ntfs.md)<br/>                                         | Verwalten von Transaktionsdateihandles in Transaktional NTFS.<br/>                                                                   |
| [Grundlegende TxF-Konzepte](txf-basic-concepts.md)<br/>                                                               | Beschreibt die Konzepte "Read Committed Consistency", "read-committed isolation" und "transactional locking" in Transactional NTFS.<br/> |
| [Programmierüberlegungen für transaktionales NTFS](programming-considerations-for-transacted-fileio-.md)<br/> | Beschreibt verschiedene Programmierüberlegungen für transaktionales NTFS.<br/>                                                      |
| [Überlegungen zur Leistung bei ntfs-Transaktionen](performance-considerations-for-transactional-ntfs.md)<br/> | Empfehlungen für optimale Dateisystemtransaktionen.<br/>                                                                     |



 

 


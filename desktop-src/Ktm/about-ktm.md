---
description: Der Kerneltransaktions-Manager (KTM) ist ein Transaktions Verwaltungsdienst. Transaktionen werden als Kernel Objekte zur Verfügung gestellt, und es werden Transaktions Verwaltungsdienste für Systemkomponenten wie Transaktions-NTFS (TxF) bereitgestellt.
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: Informationen zu KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1c477c7f9ae54b86fcee03435310416b38ea8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050488"
---
# <a name="about-ktm"></a>Informationen zu KTM

Der Kerneltransaktions-Manager (KTM) ist ein Transaktions Verwaltungsdienst. Transaktionen werden als Kernel Objekte zur Verfügung gestellt, und es werden Transaktions Verwaltungsdienste für Systemkomponenten wie [Transaktions-NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF) bereitgestellt.

In den folgenden Themen werden die Verwendungsmöglichkeiten und Funktionen von KTM beschrieben:

-   [Was ist eine Transaktion?](what-is-a-transaction.md)
-   [Arbeiten mit Transaktionen](programming-model.md)
-   [Schreiben einer Ressourcen-Manager](writing-a-resource-manager.md)
-   [Interoperabilität mit anderen Windows-Features](interoperability-with-other-windows-features.md)
-   [Sicherheit und Zugriffsrechte für KTM](ktm-security-and-access-rights.md)

KTM basiert auf der [gemeinsames Protokolldateisystem](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) für seinen Vorgang. CLFS ist ein Protokollierungs System, das Transaktionen aktivieren kann.

 

 

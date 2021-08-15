---
title: Veröffentlichen unter einem Computerobjekt
description: In der Regel erstellen hostbasierte Dienste SCPs unter dem Computerobjekt für den Hostcomputer. Hostbasierte Dienste sind Dienste, die eng an einen einzelnen Hostcomputer gebunden sind.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac659ab2bf482ee6d6c57dd1481e487d6e2af95dfd85a092f48f4928499b102
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025358"
---
# <a name="publishing-under-a-computer-object"></a>Veröffentlichen unter einem Computerobjekt

In der Regel erstellen hostbasierte Dienste SCPs unter dem Computerobjekt für den Hostcomputer. Hostbasierte Dienste sind Dienste, die eng an einen einzelnen Hostcomputer gebunden sind.

**So erstellen Sie SCPs unter einem Computerobjekt**

1.  Rufen Sie die [**GetComputerObjectName-Funktion**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) auf, um den Distinguished Name (DN) im Verzeichnis des Computerobjekts für den lokalen Computer abzurufen.
2.  Verwenden Sie diesen DN, um eine Bindung an das Computerobjekt herzustellen und den SCP zu erstellen.

Weitere Informationen und ein Codebeispiel finden Sie unter [Suchen und Verwenden eines Dienstverbindungspunkts](how-clients-find-and-use-a-service-connection-point.md)durch Clients.

Beachten Sie, dass nur Computer, die Mitglied der Domäne sind, über gültige Computerobjekte im Verzeichnis verfügen.

Rufen Sie die [**GetComputerNameEx-Funktion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) auf, um den DNS- oder NetBIOS-Namen des lokalen Computers abzurufen.

 

 
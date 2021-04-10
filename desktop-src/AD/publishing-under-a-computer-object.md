---
title: Veröffentlichen unter einem Computer Objekt
description: In der Regel erstellen Host basierte Dienste SCPs unter dem Computer Objekt für den Host Computer. Host basierte Dienste sind Dienste, die eng an einen einzelnen Host Computer gebunden sind.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858127"
---
# <a name="publishing-under-a-computer-object"></a>Veröffentlichen unter einem Computer Objekt

In der Regel erstellen Host basierte Dienste SCPs unter dem Computer Objekt für den Host Computer. Host basierte Dienste sind Dienste, die eng an einen einzelnen Host Computer gebunden sind.

**So erstellen Sie SCPs unter einem Computer Objekt**

1.  Aufrufen der Funktion [**getcomputerobjectname**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) , um den Distinguished Name (DN) im Verzeichnis des Computer Objekts für den lokalen Computer abzurufen.
2.  Verwenden Sie diesen DN zum Binden an das Computer Objekt und zum Erstellen des Dienst Verbindungs Punkts.

Weitere Informationen und ein Codebeispiel finden Sie unter Gewusst wie: Suchen [und Verwenden eines Dienst Verbindungs Punkts durch Clients](how-clients-find-and-use-a-service-connection-point.md).

Beachten Sie, dass nur Domänen Mitglieds Computer über gültige Computer Objekte im Verzeichnis verfügen.

Um den DNS-oder NetBIOS-Namen des lokalen Computers abzurufen, müssen Sie die Funktion [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) aufrufen.

 

 
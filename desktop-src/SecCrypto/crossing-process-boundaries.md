---
description: Die Schannel-Protokoll-Engine führt den Handshaking und die Authentifizierung in einem sicheren Prozess und die Massenverschlüsselung/Nachrichtenübergabe im Anwendungsprozess durch.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Überschreiten von Prozessgrenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f8ba4c2d7a0a80ad97e62487421b5b4a0a6f8deda9d8edb550c2d8fcddab15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768874"
---
# <a name="crossing-process-boundaries"></a>Überschreiten von Prozessgrenzen

Die [*Schannel-Protokoll-Engine*](../secgloss/s-gly.md) führt den Handshaking und die Authentifizierung in einem sicheren [*Prozess*](../secgloss/p-gly.md) und die Massenverschlüsselung/Nachrichtenübergabe im Anwendungsprozess durch. Dies bedeutet, dass die [*Massenverschlüsselungsschlüssel*](../secgloss/b-gly.md) und [*MAC-Schlüssel*](../secgloss/m-gly.md) von einem Prozess in einen anderen kopiert werden müssen. Um die Schlüssel von einem Prozess in einen anderen zu kopieren, verwenden Sie die Funktionen [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) und [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) wie folgt:

1.  Der sichere Prozess exportiert jeden Schlüssel mithilfe von [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)in eine [*OPAQUEKEYBLOB-Datei*](../secgloss/o-gly.md) und zerstört den Schlüssel dann mithilfe von [**CryptDestroyKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) Beachten Sie Folgendes: Wenn der Schlüssel auf Hardware gespeichert ist, muss der CSP dies erkennen und nicht versuchen, den Schlüssel zu zerstören.
2.  Der sichere Prozess übergibt die OPAQUEKEYBLOBs auf eine Weise, die den Rahmen dieses Dokuments sprengen kann, an den Anwendungsprozess.
3.  Der Anwendungsprozess importiert alle OPAQUEKEYBLOB-Dateien mithilfe von [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)wieder in den CSP. An diesem Punkt muss sich der Schlüssel genau im selben [*Zustand*](../secgloss/s-gly.md) wie beim Export befinden.

 

 

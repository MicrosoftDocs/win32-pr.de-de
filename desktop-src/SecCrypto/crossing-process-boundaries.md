---
description: Die SChannel-Protokoll-Engine führt das Hand Shake und die Authentifizierung in einem sicheren Prozess durch und die Massen Verschlüsselung/-Nachricht, die in den Anwendungsprozess übergeht.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Überschreiten von Prozess Grenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046bc6f53d609ec22ed37edd08d6967cc4ae73e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350408"
---
# <a name="crossing-process-boundaries"></a>Überschreiten von Prozess Grenzen

Die [*SChannel*](../secgloss/s-gly.md) -Protokoll-Engine führt das Hand Shake und die Authentifizierung in einem sicheren [*Prozess*](../secgloss/p-gly.md) durch und die Massen Verschlüsselung/-Nachricht, die in den Anwendungsprozess übergeht. Dies bedeutet, dass die [*Massen Verschlüsselungsschlüssel*](../secgloss/b-gly.md) und [*Mac*](../secgloss/m-gly.md) -Schlüssel von einem Prozess in einen anderen kopiert werden müssen. Um die Schlüssel von einem Prozess in einen anderen zu kopieren, verwenden Sie die Funktionen [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) und [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) wie folgt:

1.  Der sichere Prozess exportiert jeden Schlüssel mithilfe von [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)in ein [*opaquekeyblob*](../secgloss/o-gly.md) und zerstört dann den Schlüssel mithilfe von [**cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey). Beachten Sie Folgendes: Wenn der Schlüssel in der Hardware gespeichert ist, muss der CSP dies erkennen, und es darf nicht versucht werden, den Schlüssel zu zerstören.
2.  Der sichere Prozess übergibt die opaquekeyblosb auf eine Weise, die über den Rahmen dieses Dokuments hinausgeht, an den Anwendungsprozess weiter.
3.  Der Anwendungsprozess importiert jedes opaquekeyblob mithilfe von [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)zurück in den CSP. An diesem Punkt muss sich der Schlüssel in demselben [*Zustand*](../secgloss/s-gly.md) befinden wie beim Exportieren.

 

 

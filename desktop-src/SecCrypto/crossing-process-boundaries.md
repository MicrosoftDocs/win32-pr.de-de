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
# <a name="crossing-process-boundaries"></a><span data-ttu-id="f3d9e-103">Überschreiten von Prozess Grenzen</span><span class="sxs-lookup"><span data-stu-id="f3d9e-103">Crossing Process Boundaries</span></span>

<span data-ttu-id="f3d9e-104">Die [*SChannel*](../secgloss/s-gly.md) -Protokoll-Engine führt das Hand Shake und die Authentifizierung in einem sicheren [*Prozess*](../secgloss/p-gly.md) durch und die Massen Verschlüsselung/-Nachricht, die in den Anwendungsprozess übergeht.</span><span class="sxs-lookup"><span data-stu-id="f3d9e-104">The [*Schannel*](../secgloss/s-gly.md) protocol engine performs the handshaking and authentication in a secure [*process*](../secgloss/p-gly.md) and the bulk encryption/message passing in the application process.</span></span> <span data-ttu-id="f3d9e-105">Dies bedeutet, dass die [*Massen Verschlüsselungsschlüssel*](../secgloss/b-gly.md) und [*Mac*](../secgloss/m-gly.md) -Schlüssel von einem Prozess in einen anderen kopiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f3d9e-105">This means that the [*bulk encryption keys*](../secgloss/b-gly.md) and [*MAC*](../secgloss/m-gly.md) keys must be copied from one process to another.</span></span> <span data-ttu-id="f3d9e-106">Um die Schlüssel von einem Prozess in einen anderen zu kopieren, verwenden Sie die Funktionen [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) und [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f3d9e-106">To copy the keys from one process to another, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) functions as follows:</span></span>

1.  <span data-ttu-id="f3d9e-107">Der sichere Prozess exportiert jeden Schlüssel mithilfe von [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)in ein [*opaquekeyblob*](../secgloss/o-gly.md) und zerstört dann den Schlüssel mithilfe von [**cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span><span class="sxs-lookup"><span data-stu-id="f3d9e-107">The secure process exports each key into an [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) using [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), then destroys the key using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span> <span data-ttu-id="f3d9e-108">Beachten Sie Folgendes: Wenn der Schlüssel in der Hardware gespeichert ist, muss der CSP dies erkennen, und es darf nicht versucht werden, den Schlüssel zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="f3d9e-108">Note that if the key is stored in hardware, the CSP must recognize this and must not attempt to destroy the key.</span></span>
2.  <span data-ttu-id="f3d9e-109">Der sichere Prozess übergibt die opaquekeyblosb auf eine Weise, die über den Rahmen dieses Dokuments hinausgeht, an den Anwendungsprozess weiter.</span><span class="sxs-lookup"><span data-stu-id="f3d9e-109">The secure process passes the OPAQUEKEYBLOBs to the application process in a manner beyond the scope of this document.</span></span>
3.  <span data-ttu-id="f3d9e-110">Der Anwendungsprozess importiert jedes opaquekeyblob mithilfe von [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)zurück in den CSP.</span><span class="sxs-lookup"><span data-stu-id="f3d9e-110">The application process imports each OPAQUEKEYBLOB back into the CSP using [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="f3d9e-111">An diesem Punkt muss sich der Schlüssel in demselben [*Zustand*](../secgloss/s-gly.md) befinden wie beim Exportieren.</span><span class="sxs-lookup"><span data-stu-id="f3d9e-111">At this point, the key must be in exactly the same [*state*](../secgloss/s-gly.md) as when it was exported.</span></span>

 

 

---
title: Zugreifen auf nicht transparente Zeiger
description: Clients können mithilfe von nicht transparenten Zeigern auf die in Zielen gespeicherten Informationen zugreifen.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b76e99a66b13c696951a0d46684726f79f29df5b0287e9c4923dc4054943e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030620"
---
# <a name="accessing-opaque-pointers"></a>Zugreifen auf nicht transparente Zeiger

Clients können mithilfe von nicht transparenten Zeigern auf die in Zielen gespeicherten Informationen zugreifen. Um den Speicher zu verwenden, muss der Client zuerst [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) aufrufen, um den Zeiger abzurufen. Wenn eine Änderung der Informationen erforderlich ist, muss der Client zuerst das Ziel sperren, indem [**er RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) aufruft, wobei der *LockDest-Parameter* auf **TRUE** festgelegt ist. Sobald das Ziel gesperrt ist, kann der Client die erforderliche Änderung vornehmen. Das Ziel kann mit einem anderen Aufruf von **RtmLockDestination** entsperrt werden, wobei der *LockDest-Parameter* auf FALSE festgelegt **ist.**

Mit der [**RtmLockDestination-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) kann ein Client auch eine Lesesperre oder eine Schreibsperre verwenden, indem der *Exclusive-Parameter* verwendet wird. Ein Client sollte die Schreibsperre nur verwenden, wenn er Änderungen an den Informationen vornimmt, die mit dem nicht transparenten Zeiger beibehalten werden. Clients können die Lesesperre verwenden, um die nicht transparenten Zeigerinformationen anzuzeigen, die in einem Ziel gespeichert sind.

Beispielcode, der zeigt, wie diese Funktionen verwendet werden, finden Sie unter [Zugreifen auf den nicht transparenten Zeiger in einem Ziel.](access-the-opaque-pointer-in-a-destination.md)

 

 





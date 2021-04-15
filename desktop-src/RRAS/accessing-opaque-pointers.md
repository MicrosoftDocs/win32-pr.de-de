---
title: Zugreifen auf nicht transparente Zeiger
description: Clients können auf die in Zielen gespeicherten Informationen mithilfe von nicht transparenten Zeigern zugreifen.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515878"
---
# <a name="accessing-opaque-pointers"></a>Zugreifen auf nicht transparente Zeiger

Clients können auf die in Zielen gespeicherten Informationen mithilfe von nicht transparenten Zeigern zugreifen. Um den Speicher zu verwenden, muss der Client zuerst [**rtmgetopaqueinformationpointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) aufrufen, um den Zeiger zu erhalten. Wenn eine Änderung an den Informationen erforderlich ist, muss der Client zunächst das Ziel durch Aufrufen von [**rtmlockdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) sperren, wobei der *Lock dest* -Parameter auf **true** festgelegt ist. Wenn das Ziel gesperrt ist, kann der Client die erforderlichen Änderungen vornehmen. Das Ziel kann mithilfe eines anderen **rtmlockdestination** -Aufrufes entsperrt werden, wobei der *Lock dest* -Parameter auf **false** festgelegt ist.

Die [**rtmlockdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) -Funktion ermöglicht es einem Client auch, mithilfe des *exklusiven* Parameters entweder eine Lesesperre oder eine Schreibsperre zu verwenden. Ein Client sollte die Schreibsperre nur dann verwenden, wenn er Änderungen an den Informationen vornimmt, die mithilfe des nicht transparenten Zeigers gespeichert werden. Clients können die Lesesperre verwenden, um die in einem Ziel gespeicherten nicht transparenten Zeiger Informationen anzuzeigen.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [zugreifen auf den nicht transparenten Zeiger in einem Ziel](access-the-opaque-pointer-in-a-destination.md).

 

 





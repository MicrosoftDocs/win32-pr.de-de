---
title: Prozedurserialisierung
description: Wenn Sie die Prozedurserialisierung verwenden, wird eine Prozedur mit dem Attribut \encode\ oder \decode\ bezeichnet. Anstatt den üblichen Remotestub zu generieren, generiert der Compiler einen Serialisierungsstub für die Routine.
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023b514aa5a2e5be1b937a3989c3446bcc6e61c76f885381ce257286b5c625b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018950"
---
# <a name="procedure-serialization"></a>Prozedurserialisierung

Wenn Sie die Prozedurserialisierung verwenden, wird eine Prozedur mit dem \[ [**Codierungs-**](/windows/desktop/Midl/encode) \] oder \[ [**Decodierungsattribut**](/windows/desktop/Midl/decode) \] bezeichnet. Anstatt den üblichen Remotestub zu generieren, generiert der Compiler einen Serialisierungsstub für die Routine.

Ebenso wie eine Remoteprozedur ein Bindungshandle verwenden muss, um einen Remoteaufruf durchzuführen, muss eine Serialisierungsprozedur ein Serialisierungshandle verwenden, um Serialisierungsdienste zu verwenden. Wenn kein Serialisierungshandle angegeben ist, wird ein implizites Standardhandle verwendet, um den Aufruf zu leiten. Wenn das Serialisierungshandle hingegen entweder als explizites [**\_ Handle-t-Argument**](/windows/desktop/Midl/handle-t) der Routine oder mithilfe des \[ [**expliziten \_ Handleattributs**](/windows/desktop/Midl/explicit-handle) angegeben \] wird, müssen Sie ein gültiges Handle als Argument des Aufrufs übergeben. Weitere Informationen zum Erstellen eines gültigen Serialisierungshandles finden Sie unter [Serialisierungshandles,](serialization-handles.md) [Beispiele für feste Puffercodierung](fixed-buffer-serialization.md)und [Beispiele für inkrementelle Codierung.](examples-of-incremental-encoding.md)

> [!Note]
> Microsoft RPC ermöglicht das Mischen von Remote- und Serialisierungsprozeduren in einer Schnittstelle. Gehen Sie dabei jedoch mit Bedacht vor.
> 
> Für Remoteprozeduren mit impliziten Bindungshandles generiert der MIDL-Compiler eine globale Handlevariable vom Typ [**handle \_ t**](/windows/desktop/Midl/handle-t). Prozeduren und Typen mit impliziten Serialisierungshandles verwenden dieselbe globale Handlevariable.
> 
> Bei impliziten Handles muss das globale implizite Handle vor einem Remoteaufruf auf ein gültiges Bindungshandle festgelegt werden. Das implizite Handle muss vor einem Serialisierungsaufruf auf ein gültiges Serialisierungshandle festgelegt werden. Daher kann eine Prozedur nicht remote und serialisiert werden. Es muss das eine oder das andere sein.

 

 

 
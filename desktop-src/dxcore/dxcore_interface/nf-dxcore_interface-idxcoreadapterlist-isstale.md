---
title: IDXCoreAdapterList::IsStale
description: Bestimmt, ob Änderungen an diesem System dazu führen, dass dieses DXCore-Adapterlistenobjekt veraltet ist.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a40a590a76773592d5442993c75149b2349880f7681d625e777d363062f5c4be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502571"
---
# <a name="idxcoreadapterlistisstale-method"></a>IDXCoreAdapterList::IsStale-Methode

Bestimmt, ob Änderungen an diesem System dazu führen, dass dieses DXCore-Adapterlistenobjekt veraltet ist. Programmieranleitungen und Codebeispiele finden Sie unter [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)(Verwenden von DXCore zum Aufzählen von Adaptern).

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a>Rückgabe

Typ: **bool**

Gibt zurück, wenn seit dem Generieren der Liste Änderungen an Systembedingungen aufgetreten sind, die dazu führen würden, dass diese `true` Adapterliste veraltet wird. Andernfalls wird `false`zurückgegeben.

## <a name="remarks"></a>Hinweise

Sie können **IsStale fragen,** um zu ermitteln, ob sich ändernde Systembedingungen dazu geführt haben, dass diese Liste veraltet ist. Wenn **IsStale** einmal zurückgegeben wird, wird die Rückgabe für die verbleibende Lebensdauer des `true` `true` DXCore-Adapterlistenobjekts zurückgegeben. Ein veraltetes Listenobjekt gilt auch dann als veraltet, wenn die Systembedingungen in einen Zustand zurückkehren, der der Liste entspricht (die gleichen Bedingungen werden jetzt wie beim ersten Erstellen der Liste erfüllt).

## <a name="see-also"></a>Weitere Informationen

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), Verwenden von DXCore zum [Auflisten von Adaptern](../dxcore-enum-adapters.md)
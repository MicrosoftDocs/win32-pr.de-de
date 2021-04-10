---
title: Mrmpeekresourceingedexermessages-Funktion (mrmresourceingedexer. h)
description: Anzeigen von Nachrichten, die von einem ressourcenindexer generiert wurden. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 87D093AE-7444-4778-8B9E-1D0D972C90E1
keywords:
- Mrmpeekresourcindexermessages-Funktions Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmPeekResourceIndexerMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45599865633afa413594be7e82b0c7ace853434b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040670"
---
# <a name="mrmpeekresourceindexermessages-function"></a>Mrmpeekresourceingedexermessages-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Anzeigen von Nachrichten, die von einem ressourcenindexer generiert wurden. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmPeekResourceIndexerMessages(
  _In_  MrmResourceIndexerHandle  indexer,
  _Out_ MrmResourceIndexerMessage **messages,
  _Out_ ULONG                     *numMsgs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Indexer* \[ in\]
</dt> <dd>

Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den ressourcenindexer identifiziert, der Nachrichten, die Sie anzeigen möchten.

</dd> <dt>

*Nachrichten* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **mrmresourceindexermessage**](mrmresourceindexermessage.md)\*\***

Ein Zeiger auf einen Zeiger auf eine [**mrmresourceindexermessage**](mrmresourceindexermessage.md). Die Funktion weist ein Array von **mrmresourceindexermessage** zu und gibt einen Zeiger auf diesen Speicher in *Nachrichten* zurück. Geben Sie den Zeiger, dessen Adresse Sie an *Nachrichten* übergeben, nicht frei.

</dd> <dt>

*nummsgs* \[ vorgenommen\]
</dt> <dd>

Typ: **ulong \** _

Die Anzahl der Nachrichten, die in _messages * zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.

## <a name="remarks"></a>Bemerkungen

Ihre APP ist nicht in der Besitz des Speichers, der in *Nachrichten* zugeordnet und zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1803, \[ nur Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ -Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Mrmresourceingedexer. h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 


---
title: MrmPeekResourceIndexerMessages-Funktion (MrmResourceIndexer.h)
description: Zeigt alle von einem Ressourcenindexer generierten Nachrichten an. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung (Package Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 87D093AE-7444-4778-8B9E-1D0D972C90E1
keywords:
- MrmPeekResourceIndexerMessages-Funktionsmenüs und andere Ressourcen
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
ms.openlocfilehash: f72325ab147656873af2bbf13d7ce1cfa47802c816dc9f14f0c6ee4f3c821683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847330"
---
# <a name="mrmpeekresourceindexermessages-function"></a>MrmPeekResourceIndexerMessages-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Zeigt alle von einem Ressourcenindexer generierten Nachrichten an. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

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

*Indexer* \[ In\]
</dt> <dd>

Typ: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den Ressourcenindexer identifiziert, der Meldungen anzeigen möchte.

</dd> <dt>

*Messages* \[ out\]
</dt> <dd>

Typ: **[ **MrmResourceIndexerMessage**](mrmresourceindexermessage.md)\*\***

Ein Zeiger auf einen Zeiger auf eine [**MrmResourceIndexerMessage.**](mrmresourceindexermessage.md) Die Funktion ordnet ein Array von **MrmResourceIndexerMessage** zu und gibt einen Zeiger auf diesen Arbeitsspeicher in Nachrichten *zurück.* Geben Sie nicht den Zeiger frei, dessen Adresse Sie an nachrichten *übergeben.*

</dd> <dt>

*numMsgs* \[ out\]
</dt> <dd>

Typ: **ULONG \***

Die Anzahl von Nachrichten, die in Nachrichten *zurückgegeben werden.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um den Erfolg oder Fehler zu bestimmen.

## <a name="remarks"></a>Hinweise

Ihre App besitzt nicht den zugeordneten und *in* Nachrichten zurückgegebenen Arbeitsspeicher. Geben Sie ihn daher nicht frei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1803 \[\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur \[ Serverdesktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 


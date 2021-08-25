---
title: MrmResourceIndexerHandle-Struktur (MrmResourceIndexer.h)
description: Stellt ein nicht transparentes Handle für ein Ressourcenindexerobjekt dar. Das Handle wird vom Betriebssystem verwaltet. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung (Package Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: E3ED8AB8-39B8-419C-9570-1CC6B2CFE8D0
keywords:
- MrmResourceIndexerHandle-Strukturmenüs und andere Ressourcen
- PMrmResourceIndexerHandle-Strukturzeigermenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmResourceIndexerHandle
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c9cd18d6c828d5f9b5187f866d8ab637dfd4d58c3da0a8569bd8c910c7e872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825690"
---
# <a name="mrmresourceindexerhandle-structure"></a>MrmResourceIndexerHandle-Struktur

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Stellt ein nicht transparentes Handle für ein Ressourcenindexerobjekt dar. Das Handle wird vom Betriebssystem verwaltet. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
typedef struct _MrmResourceIndexerHandle {
  PVOID handle;
} MrmResourceIndexerHandle, *PMrmResourceIndexerHandle;
```



## <a name="members"></a>Member

<dl> <dt>

**Handlebezeichner**
</dt> <dd>

Typ: **PVOID**

</dd> <dd>

Ein nicht transparentes Handle für ein Ressourcenindexerobjekt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1803 desktop apps only (Nur \[ Desktop-Apps der Version 1803)\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur \[ Serverdesktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 


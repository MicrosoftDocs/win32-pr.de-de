---
title: Mrmresourceindexermessage-Struktur (mrmresourceindexer. h)
description: Stellt eine Meldung dar, die von einem ressourcenindexer generiert wurde. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: E00065E6-A468-4ACD-AF89-434E4F5025A4
keywords:
- Mrmresourceindexermessage-Struktur Menüs und weitere Ressourcen
- Pmrmresourceindexermessage-Struktur Zeiger Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessage
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5073c4f74852d341d7f0711a34abe4459dcbaa79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949555"
---
# <a name="mrmresourceindexermessage-structure"></a>Mrmresourceindexermessage-Struktur

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Stellt eine Meldung dar, die von einem ressourcenindexer generiert wurde. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
typedef struct _MrmResourceIndexerMessage {
  MrmResourceIndexerMessageSeverity severity;
  ULONG                             id;
  PCWSTR                            text;
} MrmResourceIndexerMessage, *PMrmResourceIndexerMessage;
```



## <a name="members"></a>Member

<dl> <dt>

**severity**
</dt> <dd>

Typ: **[ **mrmresourceindexermessageseverity**](mrmresourceindexermessageseverity.md)**

</dd> <dd>

Ein-Wert, der den Schweregrad der Nachricht angibt.

</dd> <dt>

**id**
</dt> <dd>

Typ: **ulong**

</dd> <dd>

Ein eindeutiger Bezeichner für die Nachricht.

</dd> <dt>

**text**
</dt> <dd>

Typ: **pcwstr**

</dd> <dd>

Der Text der Meldung. Diesen Zeiger nicht freigeben; der Arbeitsspeicher befindet sich im Besitz des Betriebssystems.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1803, \[ nur Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ -Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Mrmresourceingedexer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 


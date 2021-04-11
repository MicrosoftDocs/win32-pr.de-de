---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess-Abfrage.
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: bd93e1cadb7da500a82218924044af79fbb1f493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127925"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Ausgabestruktur

Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) -Abfrage.

Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT          Output;
  UINT                                          ProcessIndex;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentifer;
  HANDLE                                        ProcessHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT;
```



## <a name="members"></a>Member

<dl> <dt>

**Ausgabe**
</dt> <dd>

Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.

</dd> <dt>

**Processindex**
</dt> <dd>

Der Index des Prozesses in der Liste der Prozesse.

</dd> <dt>

**Processidentifer**
</dt> <dd>

Ein [**D3DAUTHENTICATEDCHANNEL \_ processidentifiertype**](d3dauthenticatedchannel-processidentifiertype.md) -Wert, der den Typ des Prozesses angibt.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Ein Prozess handle. Wenn der **processidentifier** -Member gleich dem **processidtype- \_ handle** ist, enthält das **ProcessHandle** -Element ein gültiges Handle für einen Prozess. Andernfalls wird dieser Member ignoriert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der DWM-Prozess (Desktopfenster-Manager) wird durch Festlegen von **processidentifier** auf **processidtype \_ DWM** identifiziert. Andere Prozesse werden identifiziert, indem das Prozess handle in **ProcessHandle** festgelegt und **processidentifier** auf **processidtype \_ handle** festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Video Strukturen](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 





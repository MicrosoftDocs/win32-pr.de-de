---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS-Abfrage.
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT-Struktur (D3d9types.h)
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
ms.openlocfilehash: a8a9f3f916dff486be01584d98bef59aa3bda4851d41e2b03f8f86819be28ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742916"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ OUTPUT-Struktur

Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS-Abfrage.**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)

Rufen Sie [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)auf, um diese Abfrage zu senden.

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

Eine [**D3DAUTHENTICATEDCHANNEL \_ QUERY \_ OUTPUT-Struktur,**](d3dauthenticatedchannel-query-output.md) die eine Nachrichtenauthentifizierungscode (MAC) und andere Daten enthält.

</dd> <dt>

**ProcessIndex**
</dt> <dd>

Der Index des Prozesses in der Liste der Prozesse.

</dd> <dt>

**ProcessIdentifer**
</dt> <dd>

Ein [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE-Wert,**](d3dauthenticatedchannel-processidentifiertype.md) der den Prozesstyp angibt.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Ein Prozesshandle. Wenn der **ProcessIdentifier-Member** **dem PROCESSIDTYPE \_ HANDLE** entspricht, enthält der **ProcessHandle-Member** ein gültiges Handle für einen Prozess. Andernfalls wird dieser Member ignoriert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Desktopfenster-Manager(DWM)-Prozess wird identifiziert, indem **ProcessIdentifier** auf **PROCESSIDTYPE \_ DWM** festgelegt wird. Andere Prozesse werden identifiziert, indem sie das Prozesshandle in **ProcessHandle** und **ProcessIdentifier** auf **PROCESSIDTYPE \_ HANDLE** festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Videostrukturen](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 





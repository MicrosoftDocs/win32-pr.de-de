---
title: WM_INDIVIDUALIZE_STATUS -Struktur (Wmdrmsdk.h)
description: Die WM \_ INDIVIDUALIZE \_ STATUS-Struktur enthält Informationen zu einem ausstehenden Individualisierungsprozess.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- WM_INDIVIDUALIZE_STATUS struktur windows media format
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c139631fe737e07d011e43920ab63c7394f03c3319abb2f7936153ae06c596ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708300"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a>WM_INDIVIDUALIZE_STATUS -Struktur (Wmdrmsdk.h)

Die **WM \_ INDIVIDUALIZE \_ STATUS-Struktur** enthält Informationen zu einem ausstehenden Individualisierungsprozess.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a>Member

<dl> <dt>

**Std.**
</dt> <dd>

**HRESULT-Rückgabecode.**

</dd> <dt>

**enIndiStatus**
</dt> <dd>

Der Wert des [**DRM \_ INDIVIDUALIZATION \_ STATUS-Enumerationstyps,**](drmdrm-individualization-status.md) der den aktuellen Status des Individualisierungsprozesses angibt.

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die die Individualisierungsantwort-URL enthält.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

Die Anzahl der abgeschlossenen HTTP-Roundtrips zum Individualisierungsdienst.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Der Wert des [**\_ DRM-HTTP \_ STATUS-Enumerationstyps.**](drmdrm-http-status.md)

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

Die Anzahl der heruntergeladenen Bytes.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

Die Gesamtzahl der bytes, die heruntergeladen werden sollen. Sie können diesen Wert und **dwHTTPReadProgress** verwenden, um eine Benutzeroberfläche anzuzeigen, die angibt, wie viel der Download abgeschlossen wurde und wie viel noch zu tun ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird empfangen, wenn Sie die [**IWMDRMIndividualizationStatus::GetStatus-Methode**](iwmdrmindividualizationstatus-getstatus.md) aufrufen. Sie enthält den Status des ausstehenden Individualisierungsprozesses zum Zeitpunkt des Aufrufs.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 






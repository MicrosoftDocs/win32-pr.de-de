---
title: WM_INDIVIDUALIZE_STATUS Struktur (wmdrmsdk. h)
description: Die WM \_ Individual \_ Status-Struktur enthält Informationen zu einem ausstehenden Individualisierungsprozess.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- WM_INDIVIDUALIZE_STATUS Struktur-Windows Media-Format
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
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369703"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a>WM_INDIVIDUALIZE_STATUS Struktur (wmdrmsdk. h)

Die **WM \_ Individual \_ Status** -Struktur enthält Informationen zu einem ausstehenden Individualisierungsprozess.

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

**HRESULT** -Rückgabecode.

</dd> <dt>

**"Endstatus"**
</dt> <dd>

Wert aus dem [**DRM- \_ \_ Status**](drmdrm-individualization-status.md) -Enumerationstyp, der den aktuellen Status des Individualisierungs Prozesses angibt.

</dd> <dt>

**pszindirespurl**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die die Antwort-URL der Individualisierung enthält.

</dd> <dt>

**dwhttprequest**
</dt> <dd>

Die Anzahl der HTTP-Roundtrips zum Individualisierungs Dienst, die abgeschlossen wurden.

</dd> <dt>

**umhttpstatus**
</dt> <dd>

Der Wert des [**DRM- \_ http-statusenumerationstyps \_**](drmdrm-http-status.md) .

</dd> <dt>

**dwhttpreadprogress**
</dt> <dd>

Die Anzahl der heruntergeladenen Bytes.

</dd> <dt>

**dwhttpreadtotal**
</dt> <dd>

Die Gesamtzahl der herunter zuladenden bytes. Sie können diesen Wert und **dwhttpreadprogress** verwenden, um eine Benutzeroberfläche anzuzeigen, die angibt, wie viel der Download abgeschlossen ist und wie viel verbleiben muss.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird empfangen, wenn Sie die [**iwmdrmindividualizationstatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md) -Methode aufrufen. Sie enthält den Status des ausstehenden Individualisierungs Prozesses zum Zeitpunkt des Aufrufes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 






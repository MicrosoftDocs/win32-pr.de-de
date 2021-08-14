---
title: WM_INDIVIDUALIZE_STATUS -Struktur (Drmexternals.h)
description: Die WM \_ INDIVIDUALIZE \_ STATUS-Struktur zeichnet den Status des Individualisierungsprozesses auf.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- WM_INDIVIDUALIZE_STATUS struktur windows media format
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb083c2a90a791099f6438f2911ac9735ecd4dada9118811aa0ff581a8db37ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699020"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a>WM_INDIVIDUALIZE_STATUS -Struktur (Drmexternals.h)

Die **WM \_ INDIVIDUALIZE \_ STATUS-Struktur** zeichnet den Status des [*Individualisierungsprozesses*](wmformat-glossary.md) auf.

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

Der Wert des [**DRM \_ INDIVIDUALIZATION \_ STATUS-Enumerationstyps.**](drm-individualization-status.md)

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die die Individualisierungsantwort-URL enthält.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

**DWORD,** das die Anzahl der abgeschlossenen HTTP-Roundtrips zum Individualisierungsdienst angibt.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Der Wert des [**\_ DRM-HTTP \_ STATUS-Enumerationstyps.**](drm-http-status.md)

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

**DWORD** mit der Anzahl der bis jetzt heruntergeladenen Bytes.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

**DWORD** mit der Gesamtzahl der herunterzuladenden Bytes. Verwenden Sie diesen Wert und **dwHTTPReadProgress,** um eine Benutzeroberfläche anzuzeigen, die angibt, wie viel der Download abgeschlossen wurde und wie viel noch zu tun ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird von den DRM-Laufzeitkomponenten ausgefüllt und an Anwendungen im *pValue-Parameter* der [**IWMStatusCallback::OnStatus-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) der Anwendung gesendet, wenn das Ereignis WMT \_ INDIVIDUALIZE entspricht. Die Anwendung empfängt dieses Ereignis mehrmals während des Downloadprozesses.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Version<br/>                  | Windows Media Format 7 SDK oder neuere Versionen des SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_DRM-HTTP-STATUS \_**](drm-http-status.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 






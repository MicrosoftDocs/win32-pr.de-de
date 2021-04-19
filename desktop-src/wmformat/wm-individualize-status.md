---
title: WM_INDIVIDUALIZE_STATUS Struktur (drmexternals. h)
description: Die WM \_ Individual- \_ Status Struktur zeichnet den Status des Individualisierungs Vorgangs auf.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- WM_INDIVIDUALIZE_STATUS Struktur-Windows Media-Format
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
ms.openlocfilehash: ddec51fbdfecd407a68b3e168a82af449decce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346313"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a>WM_INDIVIDUALIZE_STATUS Struktur (drmexternals. h)

Die **WM \_ Individual- \_ Status** Struktur zeichnet den Status des [*Individualisierungs*](wmformat-glossary.md) Vorgangs auf.

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

Der Wert des DRM-Enumerationstyps für den [**\_ Individualisierungs \_ Status**](drm-individualization-status.md) .

</dd> <dt>

**pszindirespurl**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die die Antwort-URL der Individualisierung enthält.

</dd> <dt>

**dwhttprequest**
</dt> <dd>

**DWORD** , das die Anzahl von HTTP-Roundtrips zum Individualisierungs Dienst angibt, die abgeschlossen wurden.

</dd> <dt>

**umhttpstatus**
</dt> <dd>

Der Wert des [**DRM- \_ http-statusenumerationstyps \_**](drm-http-status.md) .

</dd> <dt>

**dwhttpreadprogress**
</dt> <dd>

**DWORD** , das die Anzahl der bis jetzt heruntergeladenen Bytes enthält.

</dd> <dt>

**dwhttpreadtotal**
</dt> <dd>

**DWORD** , das die Gesamtzahl der herunter zuladenden Bytes enthält. Verwenden Sie diesen Wert und **dwhttpreadprogress** , um eine Benutzeroberfläche anzuzeigen, die angibt, wie viel der Download abgeschlossen ist und wie viel verbleiben muss.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird von den DRM-Laufzeitkomponenten ausgefüllt und an Anwendungen im *pValue* -Parameter der Anwendung [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode gesendet, wenn das Ereignis gleich WMT \_ Individual ist. Die Anwendung empfängt dieses Ereignis mehrmals während des Downloadvorgangs.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Version<br/>                  | SDK für Windows Media-Format 7 oder höhere Versionen des SDKs<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM- \_ http- \_ Status**](drm-http-status.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 






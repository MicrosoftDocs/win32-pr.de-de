---
title: WM_GET_LICENSE_DATA-Struktur (Drmexternals.h)
description: Die WM \_ GET \_ LICENSE \_ DATA-Struktur enthält Informationen zum Erwerb einer DRM-Lizenz.
ms.assetid: 7e8053d5-f3f5-4519-97f5-6dbd89982f3a
keywords:
- WM_GET_LICENSE_DATA Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- WM_GET_LICENSE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f53b6ddfd532710e712637c57785d8893d8f977807bfb45cac0fc787ccbf58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844474"
---
# <a name="wm_get_license_data-structure"></a>WM \_ GET \_ LICENSE \_ DATA-Struktur

Die **WM GET LICENSE \_ \_ \_ DATA-Struktur** enthält Informationen dazu, wo eine [*DRM-Lizenz*](wmformat-glossary.md) [](wmformat-glossary.md)erworben werden kann.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WMGetLicenseData {
  DWORD   dwSize;
  HRESULT hr;
  WCHAR   *wszURL;
  WCHAR   *wszLocalFilename;
  BYTE    *pbPostData;
  DWORD   dwPostDataSize;
} WM_GET_LICENSE_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**dwSize**
</dt> <dd>

**DWORD,** das die Größe der **WM GET LICENSE \_ \_ \_ DATA-Struktur** in Bytes enthält.

</dd> <dt>

**Std.**
</dt> <dd>

**HRESULT-Rückgabecode.**

</dd> <dt>

**wszURL**
</dt> <dd>

Auf NULL endende Zeichenfolge mit Breitzeichen, die die Lizenzerwerbs-URL enthält. Verwenden Sie diese Zeichenfolge und die **pbPostData-Zeichenfolge** beim nicht automatischen Lizenzerwerb.

</dd> <dt>

**wszLocalFilename**
</dt> <dd>

Auf NULL endende Zeichenfolge mit Breitzeichen, die eine lokale HTML-Seite enthält, die von der DRM-Komponente generiert wird. Wenn diese Zeichenfolge in einen Browser geladen wird, leitet sie die HTTP-Anforderung zusammen mit den erforderlichen Postdaten automatisch an die Lizenzerwerbs-URL um. Die Verwendung dieser lokalen URL ist jetzt veraltet. Es wird empfohlen, die **Zeichenfolgen wszURL** und **pbPostData** zu verwenden.

</dd> <dt>

**pbPostData**
</dt> <dd>

Zeiger auf ein Bytearray, das die Daten enthält, die an die Lizenzerwerbs-URL gesendet werden sollen. Sie müssen am Anfang der **pbPostData-Zeichenfolge** die folgende Zeichenfolge hinzufügen: "nonsilent=1&challenge=". Die resultierende Zeichenfolge sollte dann beim Erstellen der HTTP-Anforderung an **wszURL** angefügt werden.

</dd> <dt>

**dwPostDataSize**
</dt> <dd>

**DWORD,** das die Größe von **pbPostData** ohne die Zeichenfolge "nonsilent=1&challenge=" angibt, auf die in **pbPostData** verwiesen wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese ausgefüllte Struktur wird im *pValue-Parameter* der [**IWMStatusCallback::OnStatus-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) zurückgegeben, wenn **WMT \_ STATUS** gleich **WMT \_ NO RIGHTS \_ \_ EX** oder **WMT ACQUIRE \_ \_ LICENSE** ist. Bei WMT \_ NO \_ RIGHTS \_ EX-Ereignissen ist das **HR-Mitglied** NS E \_ LICENSE \_ \_ REQUIRED, NS \_ E LICENSE \_ \_ OUTOFDATE oder NS \_ E LICENSE INCORRECT \_ \_ \_ RIGHTS. Jeder dieser Fehler gibt an, dass eine neue Lizenz erworben werden muss, indem Sie zur URL im **wszURL-Mitglied** navigieren.

Bei WMT \_ ACQUIRE \_ LICENSE-Ereignissen übergibt das **hr-Mitglied** das SUCCEEDED-Makro, wenn eine Lizenz erfolgreich erworben wurde. Wenn dieses Ereignis nach einem Versuch der automatischen Übernahme empfangen wird und **hr** gleich NS \_ E \_ DRM LICENSE \_ \_ NOTACQUIRED ist, gibt dies an, dass nur der nicht automatische Erwerb vom Lizenzserver für diese Lizenz unterstützt wird.

Die Audioplayer-Beispielanwendung veranschaulicht, wie die in dieser Struktur zurückgegebenen Informationen ordnungsgemäß verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Version<br/>                  | Windows Media Format 7 SDK oder höhere Versionen des SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 






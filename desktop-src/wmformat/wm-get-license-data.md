---
title: WM_GET_LICENSE_DATA Struktur (drmexternals. h)
description: Die WM \_ - \_ Lizenz \_ Datenstruktur enthält Informationen darüber, wo eine DRM-Lizenz abgerufen werden muss.
ms.assetid: 7e8053d5-f3f5-4519-97f5-6dbd89982f3a
keywords:
- WM_GET_LICENSE_DATA Struktur-Windows Media-Format
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
ms.openlocfilehash: 4f238bea29ab7271896dc7516b6424e4cc298f5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391905"
---
# <a name="wm_get_license_data-structure"></a>WM \_ - \_ Lizenz \_ Datenstruktur erhalten

Die **WM \_ - \_ Lizenz \_ Daten** Struktur enthält Informationen darüber, wo eine [*DRM*](wmformat-glossary.md) - [*Lizenz*](wmformat-glossary.md)abgerufen werden muss.

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

**DWORD** , das die Größe der **WM-Lizenz für die \_ get- \_ Lizenz \_ Daten** in Bytes enthält.

</dd> <dt>

**Std.**
</dt> <dd>

**HRESULT** -Rückgabecode.

</dd> <dt>

**wszurl**
</dt> <dd>

Eine mit NULL endenden breit Zeichen-Zeichenfolge, die die Lizenz Erwerbs-URL enthält. Verwenden Sie diese Zeichenfolge und die **pbpostdata** -Zeichenfolge in einem nicht automatischen Lizenzerwerb.

</dd> <dt>

**wszlocalfilename**
</dt> <dd>

Breit Zeichen-NULL-terminierte Zeichenfolge, die eine lokale HTML-Seite enthält, die von der DRM-Komponente generiert wird. Wenn diese Zeichenfolge in einen Browser geladen wird, wird die HTTP-Anforderung zusammen mit den erforderlichen Post-Daten automatisch an die Lizenz Erwerbs-URL umgeleitet. Die Verwendung dieser lokalen URL ist nun veraltet. Die empfohlene Vorgehensweise ist die Verwendung der **wszurl** -und **pbpostdata** -Zeichen folgen.

</dd> <dt>

**pbpostdata**
</dt> <dd>

Zeiger auf ein Bytearray, das die Daten enthält, die an die Lizenz Erwerbs-URL gesendet werden sollen. Sie müssen die folgende Zeichenfolge am Anfang der **pbpostdata** -Zeichenfolge hinzufügen: "nonsilent = 1&Challenge =". Die resultierende Zeichenfolge sollte dann an **wszurl** angehängt werden, wenn Sie die HTTP-Anforderung bilden.

</dd> <dt>

**dwpostdatasize**
</dt> <dd>

**DWORD** , das die Größe von **pbpostdata** ohne die Zeichenfolge "nonsilent = 1&Challenge =" angibt, auf die in **pbpostdata** verwiesen wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese ausgefüllte Struktur wird im *pValue* -Parameter der [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode zurückgegeben, wenn der **WMT- \_ Status** " **WMT \_ No \_ Rights \_ Ex** " oder " **WMT-Abruf \_ \_ Lizenz**" entspricht. Für WMT \_ - \_ Ereignisse ohne Rechte \_ Ereignisse ist das **HR** -Mitglied NS \_ e- \_ Lizenz \_ erforderlich, NS e-Lizenz- \_ \_ \_ oudefdate oder NS e- \_ \_ Lizenz \_ falsche \_ Rechte. Jeder dieser Fehler gibt an, dass eine neue Lizenz abgerufen werden muss, indem zur URL im **wszurl** -Member navigiert wird.

Beim Abrufen von \_ Lizenz Ereignissen durch WMT \_ übergibt das **Personal** Mitglied das Makro "erfolgreich", wenn eine Lizenz erfolgreich abgerufen wurde. Wenn dieses Ereignis nach einem Versuch der automatischen Übernahme empfangen wird und **HR** gleich der NS \_ E \_ DRM- \_ Lizenz \_ notbezogen ist, bedeutet dies, dass nur nicht automatische Käufe vom Lizenzserver für diese Lizenz unterstützt werden.

Die Audioplayer-Beispielanwendung veranschaulicht, wie die in dieser Struktur zurückgegebenen Informationen ordnungsgemäß verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Version<br/>                  | SDK für Windows Media-Format 7 oder höhere Versionen des SDKs<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmreader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 






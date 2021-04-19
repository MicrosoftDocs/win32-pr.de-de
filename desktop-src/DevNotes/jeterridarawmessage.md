---
description: Ruft eine unformatierte Meldungs Zeichenfolge ab, wenn ein Fehlercode Bezeichner (IDA) bereitgestellt wird.
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: Jeterridarawmessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369239"
---
# <a name="jeterridarawmessage-function"></a>Jeterridarawmessage-Funktion

Ruft eine unformatierte Meldungs Zeichenfolge ab, wenn ein Fehlercode Bezeichner (IDA) bereitgestellt wird.

## <a name="syntax"></a>Syntax


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*I* 
</dt> <dd>

Eine Zahl, die einem bestimmten Fehlercode zugeordnet ist und dem Benutzer angezeigt wird.

</dd> <dt>

*pMessage* 
</dt> <dd>

Ein Zeiger auf die Fehlermeldung.

</dd> <dt>

*cbmessage* 
</dt> <dd>

Gibt die Anzahl der Bytes in der Fehlermeldung an.

</dd> <dt>

*pcbactual* 
</dt> <dd>

Ein Zeiger auf die tatsächliche Anzahl der gelesenen Bytes.

</dd> <dt>

*pcontextid* 
</dt> <dd>

Ein Zeiger auf den Kontext Bezeichner, der der Hilfedatei zugeordnet ist.

</dd> <dt>

*pwszhelp/Datei* 
</dt> <dd>

Ein Zeiger auf einen Zeiger auf die Datei, in der der Fehler erläutert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie **Jet \_ errsuccess** zurück; andernfalls wird eine nicht formatierte Meldung zurückgegeben, die die Ursache für den Fehler angibt.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 

---
description: Ruft bei Bereitstellung eines Jet-Fehlers einen Fehlercode Bezeichner (IDA) und eine unformatierte Meldungs Zeichenfolge ab.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: Jeterrrawmessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357935"
---
# <a name="jeterrrawmessage-function"></a>Jeterrrawmessage-Funktion

Ruft bei Bereitstellung eines Jet-Fehlers einen Fehlercode Bezeichner (IDA) und eine unformatierte Meldungs Zeichenfolge ab.

## <a name="syntax"></a>Syntax


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*irre* 
</dt> <dd>

Der Jet-Fehler, der den erhaltenen Informationen entspricht.

</dd> <dt>

*pida* 
</dt> <dd>

Ein Zeiger auf die IDA.

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

Verweist auf einen Zeiger auf die Datei, in der der Fehler erläutert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie **Jet \_ errsuccess** zurück; andernfalls wird eine unformatierte Fehlermeldung zurückgegeben, die die Ursache für den Fehler angibt.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 

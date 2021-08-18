---
description: Ruft einen Fehlercodebezeichner (IDA) und eine unformatierte Meldungszeichenfolge ab, wenn ein Jet-Fehler bereitgestellt wird.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: JetErrRawMessage-Funktion
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
ms.openlocfilehash: efc7332530b5b03b0c9150adb8b0e105d0e5d17eeae9bbc485fb073391de2cad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749680"
---
# <a name="jeterrrawmessage-function"></a>JetErrRawMessage-Funktion

Ruft einen Fehlercodebezeichner (IDA) und eine unformatierte Meldungszeichenfolge ab, wenn ein Jet-Fehler bereitgestellt wird.

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

*Err* 
</dt> <dd>

Der Jet-Fehler, der den abgerufenen Informationen entspricht.

</dd> <dt>

*Pida* 
</dt> <dd>

Ein Zeiger auf die IDA.

</dd> <dt>

*pMessage* 
</dt> <dd>

Ein Zeiger auf die Fehlermeldung.

</dd> <dt>

*cbMessage* 
</dt> <dd>

Die Anzahl der Bytes in der Fehlermeldung.

</dd> <dt>

*actual* 
</dt> <dd>

Ein Zeiger auf die tatsächliche Anzahl der gelesenen Bytes.

</dd> <dt>

*pContextId* 
</dt> <dd>

Ein Zeiger auf den Kontextbezeichner, der der Hilfedatei zugeordnet ist.

</dd> <dt>

*pwszHelp/file* 
</dt> <dd>

Zeigt auf einen Zeiger auf die Datei, die den Fehler erklärt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **JET \_ errSuccess** zurückgegeben. Andernfalls wird eine unformatierte Fehlermeldung zurückgegeben, die den spezifischen Grund für den Fehler angibt.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 

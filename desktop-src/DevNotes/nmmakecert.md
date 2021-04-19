---
description: Erstellt ein Benutzerzertifikat für die Verwendung mit NetMeeting-Konferenzen.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: Nmmakecert-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359646"
---
# <a name="nmmakecert-function"></a>Nmmakecert-Funktion

Erstellt ein Benutzerzertifikat für die Verwendung mit NetMeeting-Konferenzen.

## <a name="syntax"></a>Syntax


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szfirstname* 
</dt> <dd>

Dies ist der Vorname des Benutzers.

</dd> <dt>

*szlastname* 
</dt> <dd>

Dies ist der Nachname des Benutzers.

</dd> <dt>

*szemailname* 
</dt> <dd>

Der e-Mail-Name des Benutzers.

</dd> <dt>

*szcity* 
</dt> <dd>

Die Stadt des Benutzers.

</dd> <dt>

*szcountry* 
</dt> <dd>

Das Land/die Region des Benutzers.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Ein Wert, der angibt, wie das Zertifikat erstellt werden soll. Die folgenden Werte sind möglich:



| Wert                                                                                                                                                                                                                                                            | Bedeutung                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <dt>**Nmmkcert \_ F \_ \_ nur**</dt> " <dt>0x00000004</dt> " bereinigen </dl>    | Löschen Sie das alte Zertifikat, ohne eine neue zu erstellen. <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <dt>**Nmmkcert \_ F \_ deleteoldcert**</dt> <dt>0x00000001</dt> </dl>  | Löschen Sie das alte Zertifikat, das zuvor mit dieser Funktion erstellt wurde. <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <dt>**Nmmkcert \_ F \_ lokaler \_ Computer**</dt> <dt>0x00000002</dt> </dl> | Erstellen Sie das Zertifikat im Zertifikat Speicher des lokalen Computers. <br/>    |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 1 zurück, wenn die Funktion erfolgreich ist, und – 1, wenn die Funktion fehlschlägt.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Nmmkcert.dll</dt> </dl> |



 

 

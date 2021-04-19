---
description: Erstellt eine Authenticode-Zeitstempel Signatur für die signierte ausführbare Datei, die in der signedcode. FileName-Eigenschaft angegeben ist.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: Signedcode. Timestamp-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359361"
---
# <a name="signedcodetimestamp-method"></a>Signedcode. Timestamp-Methode

\[Die **timestamp** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **timestamp** -Methode erstellt eine Authenticode-Zeitstempel Signatur für die signierte ausführbare Datei, die in der **signedcode. filename** -Eigenschaft angegeben ist. Dieser Zeitstempel ist eine gegen Signatur der signierten ausführbaren Datei, die von einer Zeitstempel Zertifizierungsstelle ausgeführt wird.

## <a name="syntax"></a>Syntax


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URL* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die die URL des Zeitstempel Servers enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Ein Zeitstempel verlängert die Gültigkeit eines Zertifikats, indem überprüft wird, ob die ausführbare Datei zum Zeitpunkt der Zeitstempel signiert wurde.

Bevor diese Methode aufgerufen werden kann, muss die signierte ausführbare Datei, die mit einem Zeitstempel versehen werden soll, in der **signedcode. filename** -Eigenschaft angegeben werden, und die [**signedcode. Sign**](signedcode-sign.md) -Methode muss zum Signieren der ausführbaren Datei aufgerufen werden.

Wenn die signierte ausführbare Datei bereits mit einem Zeitstempel versehen ist, überschreibt diese Methode den vorhandenen Zeitstempel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signedcode**](signedcode.md)
</dt> </dl>

 

 

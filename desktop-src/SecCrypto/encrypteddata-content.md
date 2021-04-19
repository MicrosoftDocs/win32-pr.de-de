---
description: Legt den zu verschlüsselnden oder zu entschlüsselnden Inhalt fest oder ruft ihn ab.
ms.assetid: fdab0f19-c69e-443b-b4b3-079d23028921
title: Verschlüsselteddata. Content (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4b873d40ed04270defe04fd59f0ce00a0f84040a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359229"
---
# <a name="encrypteddatacontent-property"></a>Verschlüsselteddata. Content (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktionen [**cryptencryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) aufzurufen, um Nachrichten zu verschlüsseln und zu entschlüsseln. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **Content** -Eigenschaft legt den zu verschlüsselnden oder zu entschlüsselnden Inhalt fest oder ruft ihn ab. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
EncryptedData.Content As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Inhalt, der verschlüsselt oder entschlüsselt werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 

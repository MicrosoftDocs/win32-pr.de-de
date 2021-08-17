---
description: Ruft den Algorithmus für die verschlüsselten Daten ab.
ms.assetid: 37bebe69-3c62-44c4-a5e5-c8cdbf087fa4
title: EncryptedData.Algorithm-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 52700a8b91495ffc9c6482b9f25265fd33f5be975032939b21571a794baea542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766716"
---
# <a name="encrypteddataalgorithm-property"></a>EncryptedData.Algorithm-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen Platform Invocation Services (PInvoke), um die Win32-API-Funktionen [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) aufzurufen, um Nachrichten zu verschlüsseln und zu entschlüsseln. Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) Die [Unterabschnitte .NET und CryptoAPI über P/Invoke: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.NET und CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Erweiterung der [.NET-Kryptografie mit CAPICOM und P/Invoke](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **Algorithm-Eigenschaft** ruft den Algorithmus für die verschlüsselten Daten ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
EncryptedData.Algorithm As Algorithm
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**Algorithm-Objekt,**](algorithm.md) das den Verschlüsselungsalgorithmus darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Encrypteddata**](encrypteddata.md)
</dt> </dl>

 

 

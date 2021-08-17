---
description: Gibt ein Zertifikat an, das zum Signieren eines Dokuments verwendet wird. Das Zertifikat kann in einer SPC-Datei (Software Publisher Certificate) oder in einem Zertifikatspeicher gespeichert werden.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: SIGNER_CERT-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: d31670575db045430e78b6c6b3182f4561b0d4784c1e1c0da95ff8629154d2c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898873"
---
# <a name="signer_cert-structure"></a>SIGNER \_ CERT-Struktur

Die **SIGNER \_ CERT-Struktur** gibt ein Zertifikat an, [*das*](../secgloss/c-gly.md) zum Signieren eines Dokuments verwendet wird. Das Zertifikat kann in einer SPC-Datei [*(Software Publisher Certificate)*](../secgloss/s-gly.md) oder in einem [*Zertifikatspeicher*](../secgloss/c-gly.md)gespeichert werden.

> [!Note]  
> Diese Struktur ist in keiner Headerdatei definiert. Um diese Struktur zu verwenden, müssen Sie sie selbst definieren, wie in diesem Thema gezeigt.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a>Member

<dl> <dt>

**cbSize**
</dt> <dd>

Die Größe der Struktur in Bytes.

</dd> <dt>

**dwCertChoice**
</dt> <dd>

Gibt an, wie das Zertifikat gespeichert wird. Bei diesem Member kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <dt>**SIGNER \_ \_ \_ ZERTIFIKATSPC-DATEI**</dt> <dt>1</dt> </dl>    | Das Zertifikat wird in einer SPC-Datei gespeichert. Der **pwszSpcFile-Member** enthält den Pfad und den Dateinamen der SPC-Datei.<br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <dt>**SIGNER \_ CERT \_ STORE**</dt> <dt>2</dt> </dl>              | Das Zertifikat wird in einem Zertifikatspeicher gespeichert. Das **pCertStoreInfo-Element** enthält einen Zeiger auf eine [**SIGNER \_ CERT \_ STORE \_ INFO-Struktur,**](signer-cert-store-info.md) die den Zertifikatspeicher angibt, in dem das Zertifikat gespeichert wird.<br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <dt>**SIGNER \_ CERT \_ SPC \_ CHAIN**</dt> <dt>3</dt> </dl> | Das Zertifikat wird in einer SPC-Datei gespeichert und einer Zertifikatkette zugeordnet. Der **pSpcChainInfo-Member** enthält einen Zeiger auf eine [**SIGNER \_ SPC \_ CHAIN \_ INFO-Struktur,**](signer-spc-chain-info.md) die die Ketteninformationen für das Zertifikat enthält.<br/> |



 

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Unicode-Zeichenfolge, die den Pfad und Dateinamen der SPC-Datei enthält, in der das Zertifikat gespeichert ist. Dieser Member wird nur verwendet, wenn der **dwCertChoice-Member** **SIGNER \_ CERT \_ SPC \_ FILE** enthält.

</dd> <dt>

**pCertStoreInfo**
</dt> <dd>

Ein Zeiger auf eine [**SIGNER \_ CERT \_ STORE \_ INFO-Struktur,**](signer-cert-store-info.md) die den Zertifikatspeicher angibt, in dem das Zertifikat gespeichert wird. Dieser Member wird nur verwendet, wenn der **dwCertChoice-Member** **SIGNER \_ CERT \_ STORE** enthält.

</dd> <dt>

**pSpcChainInfo**
</dt> <dd>

Ein Zeiger auf eine [**SIGNER \_ SPC \_ CHAIN \_ INFO-Struktur,**](signer-spc-chain-info.md) die die Ketteninformationen für das Zertifikat enthält. Dieser Member wird nur verwendet, wenn der **dwCertChoice-Member** **SIGNER \_ CERT \_ SPC \_ CHAIN** enthält.

</dd> <dt>

**Hwnd**
</dt> <dd>

Das Handle des Fensters, das als Besitzer aller angezeigten Dialogfelder verwendet werden soll. Dieser Member wird derzeit nicht verwendet und ignoriert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 

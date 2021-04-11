---
description: Gibt ein Zertifikat an, das zum Signieren eines Dokuments verwendet wird. Das Zertifikat kann in einer SPC-Datei (Software Publisher Certificate) oder in einem Zertifikat Speicher gespeichert werden.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: SIGNER_CERT Struktur
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
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217619"
---
# <a name="signer_cert-structure"></a>Signatur Geber- \_ Zertifikat Struktur

Die **Signatur Geber \_** -Zertifikat Struktur gibt ein [*Zertifikat*](../secgloss/c-gly.md) an, das zum Signieren eines Dokuments verwendet wird. Das Zertifikat kann in einer SPC-Datei ( [*Software Publisher Certificate*](../secgloss/s-gly.md) ) oder in einem [*Zertifikat Speicher*](../secgloss/c-gly.md)gespeichert werden.

> [!Note]  
> Diese Struktur ist nicht in einer Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.

 

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

**CBSIZE**
</dt> <dd>

Die Größe der-Struktur in Bytes.

</dd> <dt>

**dwcertchoice**
</dt> <dd>

Gibt an, wie das Zertifikat gespeichert wird. Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <dt>**Signatur \_ Geber CERT \_ SPC- \_ Datei**</dt> <dt>1</dt> </dl>    | Das Zertifikat wird in einer SPC-Datei gespeichert. Der Member " **pwszspcfile** " enthält den Pfad und den Dateinamen der SPC-Datei.<br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <dt>**Signatur \_ Geber Zertifikat \_ Speicher**</dt> <dt>2</dt> </dl>              | Das Zertifikat wird in einem Zertifikat Speicher gespeichert. Das **pcertstoreinfo** -Element enthält einen Zeiger auf eine Signatur Geber-Zertifikat [**\_ Speicher- \_ \_ Informations**](signer-cert-store-info.md) Struktur, die den Zertifikat Speicher angibt, in dem das Zertifikat gespeichert ist.<br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <dt>**Signatur \_ Geber Zertifikat- \_ SPC- \_ Kette**</dt> <dt>3</dt> </dl> | Das Zertifikat wird in einer SPC-Datei gespeichert und mit einer Zertifikat Kette verknüpft. Das **pspcchaininfo** -Element enthält einen Zeiger auf eine Signatur Geber- [**\_ SPC- \_ Ketten \_ Info**](signer-spc-chain-info.md) -Struktur, die die Ketten Informationen für das Zertifikat enthält.<br/> |



 

</dd> <dt>

**pwszspcfile**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Pfad und den Dateinamen der SPC-Datei enthält, in der das Zertifikat gespeichert ist. Dieser Member wird nur verwendet, wenn das **dwcertchoice** -Element eine Signatur Geber- **Zertifikat-SPC- \_ \_ \_ Datei** enthält.

</dd> <dt>

**pcertstoreingefo**
</dt> <dd>

Ein Zeiger auf eine Signatur Geber-Zertifikat [**\_ \_ Speicher \_ Info**](signer-cert-store-info.md) -Struktur, die den Zertifikat Speicher angibt, in dem das Zertifikat gespeichert ist. Dieser Member wird nur verwendet, wenn das **dwcertchoice** -Element den Signatur Geber- **\_ Zertifikat \_ Speicher** enthält.

</dd> <dt>

**pspcchaininfo**
</dt> <dd>

Ein Zeiger auf die Informationsstruktur der Signatur Geber- [**\_ SPC- \_ Kette \_**](signer-spc-chain-info.md) , die die Ketten Informationen für das Zertifikat enthält. Dieser Member wird nur verwendet, wenn der **dwcertchoice** -Member eine Signatur Geber- **Zertifikat-SPC- \_ \_ \_ Kette** enthält.

</dd> <dt>

**HWND**
</dt> <dd>

Das Handle des Fensters, das als Besitzer beliebiger Dialogfelder verwendet werden soll, die angezeigt werden. Dieser Member wird derzeit nicht verwendet und wird ignoriert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signersign**](signersign.md)
</dt> <dt>

[**Signersignetx**](signersignex.md)
</dt> </dl>

 

 

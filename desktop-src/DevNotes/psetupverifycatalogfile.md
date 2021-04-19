---
description: Überprüft eine einzelne Katalog Datei mithilfe der Standard Code Signatur Richtlinie des Betriebssystems, z. b. Treiber Signatur.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: psetupverifycatalogfile-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366898"
---
# <a name="psetupverifycatalogfile-function"></a>psetupverifycatalogfile-Funktion

\[Diese Funktion wird von Microsoft nicht mehr unterstützt. Für eine INF-Datei (Geräteinstallation) sollten Entwickler **setupverifyinffile** verwenden. Verwenden Sie zum Überprüfen eines nicht-INF-basierten Katalogs **WinVerifyTrust**.\]

Überprüft eine einzelne Katalog Datei mithilfe der Standard Code Signatur Richtlinie des Betriebssystems, z. b. Treiber Signatur.

## <a name="syntax"></a>Syntax


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Catalogfullpath* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad der Katalog Datei, die überprüft werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird ein **Fehler \_ Erfolg** zurückgegeben; andernfalls wird der Fehler von [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Setupverifyinffile**](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 

---
description: Installiert eine Katalog Datei.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: psetupinstallcatalog-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352027"
---
# <a name="psetupinstallcatalog-function"></a>psetupinstallcatalog-Funktion

\[Diese Funktion wird von Microsoft nicht mehr unterstützt. Entwickler sollten **cryptchart adminaddcatalog** verwenden.\]

Installiert eine Katalog Datei.

## <a name="syntax"></a>Syntax


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Catalogfullpath* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad des Katalogs, der auf dem System installiert werden soll.

</dd> <dt>

*Newbasename* \[ in\]
</dt> <dd>

Der neue Basis Name, der verwendet werden soll, wenn die Katalog Datei in den Katalog Speicher kopiert wird.

</dd> <dt>

*Newcatalogfullpath* \[ Out, optional\]
</dt> <dd>

Empfängt optional den voll qualifizierten Pfad der Katalog Datei im Katalog Speicher. Dieser Puffer muss mindestens eine maximale Anzahl von **\_ Pfad** bytes (ANSI-Version) oder "Zeichen" (Unicode-Version) aufweisen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **kein \_ Fehler** zurückgegeben; andernfalls wird ein Win32-Fehlercode zurückgegeben, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Die Datei wird vom System in ein spezielles Verzeichnis kopiert und optional umbenannt.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cryptder adminaddcatalog**](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 

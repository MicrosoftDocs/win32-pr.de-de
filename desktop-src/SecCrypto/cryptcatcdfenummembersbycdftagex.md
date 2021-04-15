---
description: Listet die einzelnen dateimember im catalogfiles-Abschnitt einer Katalog Definitionsdatei (CDF) auf.
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: Crypttorcdfenumschlag mitgliedsbycdftagex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525733"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a>Crypttorcdfenumschlag mitgliedsbycdftagex-Funktion

\[Die Funktion " **cryptccdfenumschlag mitgliedsbycdftagex** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Die Funktion **cryptingcdfenummitgliedsbycdftagex** listet die einzelnen dateimember im Abschnitt **catalogfiles** einer Katalog Definitionsdatei (CDF) auf. **Crypt-cdfenumschlag-mitgliedsbycdftagex** wird von [MakeCat](makecat.md)aufgerufen.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PCDF* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**cryptstreamcdf**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) -Struktur.

</dd> <dt>

*pwszprevcdftag* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine **null**-terminierte Zeichenfolge, die das Katalog dateimember identifiziert.

</dd> <dt>

*pfnparser-Fehler* \[ in\]
</dt> <dd>

Ein Zeiger auf eine benutzerdefinierte Funktion zum Behandeln von Dateianalyse Fehlern.

</dd> <dt>

*ppmember* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**cryptsinmember**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) -Struktur, die die dateimember-Informationen enthält.

</dd> <dt>

Fehler bei " *f* \[ " in\]
</dt> <dd>

Ein-Wert, der angibt, ob im Arbeitsspeicher ein Verweis auf den letzten Enumerationsmember aufbewahrt werden soll.

</dd> <dt>

*pvReserved* \[ in\]
</dt> <dd>

Dieser Parameter ist reserviert. Verwenden Sie Sie nicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Funktion einen Zeiger auf eine mit **null** endenden Zeichenfolge zurück, die ein dateimember im **catalogfiles** -Abschnitt einer CDF identifiziert. Wenn ein Fehler auftritt, gibt die Funktion " **cryptstreamcdfenummitgliedsbycdftagex** " einen **null** -Zeiger zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird in der Regel in einer Schleife aufgerufen, um alle Katalog dateimember in einer CDF aufzulisten. Legen Sie *pwszprevcdftag* vor der Eingabe der Schleife auf **null** fest. Die-Funktion gibt einen Zeiger auf das erste Element zurück. Legen Sie *pwszprevcdftag* auf den Rückgabewert der Funktion für nachfolgende Iterationen der Schleife fest.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die korrekte Reihenfolge der Zuweisungen für den *pwszprevcdftag* -Parameter ( `pwszMemberTag` ).


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**Cryptalisicdf**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**Cryptkatamember**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 

---
description: Listet die Attribute der Element Dateien im catalogfiles-Abschnitt einer Katalog Definitionsdatei (CDF) auf.
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: Cryptovcdfenumschlag attributeswithcdftag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: bd3c5905c57d234d42cd89d18c2a141c4026250f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525730"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a>Cryptovcdfenumschlag attributeswithcdftag-Funktion

\[Die Funktion " **cryptccdfenumschlag attributeswithcdftag** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Die Funktion **crypt-cdfenumattributeswithcdftag** listet die Attribute der Element Dateien im Abschnitt **catalogfiles** einer Katalog Definitionsdatei (CDF) auf. **Crypt-cdfenüberattributeswithcdftag** wird von [MakeCat](makecat.md)aufgerufen.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PCDF* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**cryptstreamcdf**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) -Struktur.

</dd> <dt>

*pwszmitgliedungstag* \[ in\]
</dt> <dd>

Ein Zeiger auf eine **null**-terminierte Zeichenfolge, die das Katalog dateimember identifiziert.

</dd> <dt>

*pmember* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**cryptsinmember**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) -Struktur, die die Element Informationen enthält.

</dd> <dt>

*pprevattr* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**cryptstreamattribute**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) -Struktur für ein dateimember-Attribut in der CDF, auf das von *PCDF* verwiesen wird.

</dd> <dt>

*pfnparser-Fehler* \[ in\]
</dt> <dd>

Ein Zeiger auf eine benutzerdefinierte Funktion zum Behandeln von Dateianalyse Fehlern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Funktion einen Zeiger auf eine [**crypttorattribute**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) -Struktur zurück. Die **cryptstreamcdfenumattributeswithcdftag** -Funktion gibt einen **null** -Zeiger zurück, wenn ein Fehler auftritt.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird in der Regel in einer Schleife aufgerufen, um alle Attribute der Katalog Dateielemente in einer CDF aufzulisten. Legen Sie *pprevattr* vor der Eingabe der Schleife auf **null** fest. Die-Funktion gibt einen Zeiger auf das erste Attribut zurück. Legen Sie *pprevattr* auf den Rückgabewert der Funktion für nachfolgende Iterationen der Schleife fest.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die korrekte Reihenfolge der Zuweisungen für den *pprevattr* -Parameter ( `pAttr` ).


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

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

[**Crypt-Attribute**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[**Cryptalisicdf**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**Cryptkatamember**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 

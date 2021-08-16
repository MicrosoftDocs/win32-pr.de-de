---
description: Führt die Attribute von Memberdateien im Abschnitt CatalogFiles einer Katalogdefinitionsdatei (CDF) auf.
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: CryptCATCDFEnumAttributesWithCDFTag-Funktion
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
ms.openlocfilehash: f1bffd01865b524b0f06003a6a46b8f81542d7f6113f98db55202e08d8dd7ee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768895"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a>CryptCATCDFEnumAttributesWithCDFTag-Funktion

\[Die **Funktion CryptCATCDFEnumAttributesWithCDFTag** steht für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Die **CryptCATCDFEnumAttributesWithCDFTag-Funktion** führt die Attribute von Memberdateien im **Abschnitt CatalogFiles** einer Katalogdefinitionsdatei (CDF) auf. **CryptCATCDFEnumAttributesWithCDFTag** wird von [MakeCat aufgerufen.](makecat.md)

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mssign32.dll.

 

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

*pCDF* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CRYPTCATCDF-Struktur.**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)

</dd> <dt>

*pwszMemberTag* \[ In\]
</dt> <dd>

Ein Zeiger auf eine mit **NULL beendete** Zeichenfolge, die das Katalogdateimitglied identifiziert.

</dd> <dt>

*pMember* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CRYPTCATMEMBER-Struktur,**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) die die Memberinformationen enthält.

</dd> <dt>

*pPrevAttr* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CRYPTCATATTRIBUTE-Struktur**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) für ein Dateimitgliedsattribut in der CDF, auf das *pCDF zeigt.*

</dd> <dt>

*pfnParseError* \[ In\]
</dt> <dd>

Ein Zeiger auf eine benutzerdefinierte Funktion zum Behandeln von Dateiparsenfehlern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Funktion einen Zeiger auf eine [**CRYPTCATATTRIBUTE-Struktur**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) zurück. Die **CryptCATCDFEnumAttributesWithCDFTag-Funktion** gibt bei einem Fehler einen **NULL-Zeiger** zurück.

## <a name="remarks"></a>Hinweise

In der Regel rufen Sie diese Funktion in einer Schleife auf, um alle Memberattribute der Katalogdatei in einer CDF aufzählen. Legen Sie *pPrevAttr* vor dem Eintritt in die Schleife auf **NULL fest.** Die Funktion gibt einen Zeiger auf das erste Attribut zurück. Legen *Sie pPrevAttr* auf den Rückgabewert der Funktion für nachfolgende Iterationen der Schleife fest.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die richtige Sequenz von Zuweisungen für den *pPrevAttr-Parameter* ( `pAttr` ).


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 

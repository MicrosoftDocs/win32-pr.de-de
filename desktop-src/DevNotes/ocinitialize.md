---
description: Initialisiert den optionalen Komponenten-Manager.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: Ocinitialize-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371022"
---
# <a name="ocinitialize-function"></a>Ocinitialize-Funktion

Initialisiert den optionalen Komponenten-Manager.

## <a name="syntax"></a>Syntax


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Rückrufe* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**OCM \_ - \_ Clientrückrufe**](ocm-client-callbacks.md) -Struktur, die die Rückruf Funktionen angibt, die vom OC-Manager zum Ausführen verschiedener Aufgaben verwendet werden sollen.

</dd> <dt>

*Masterocinfname* \[ in\]
</dt> <dd>

Der Pfad der "OC. inf"-Master Datei.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.

<dl> <dt>

<span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**Ocinit \_ Forcenewinf** (0x00000001)
</dt> <dt>

<span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**Ocinit \_ Killsubcomps** (0x00000002)
</dt> <dt>

<span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**Ocinit \_ Runquiet** (0x00000004)
</dt> <dt>

<span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**Ocinit \_ Languageaware** (0x00000008)
</dt> </dl> </dd> <dt>

*ShowError* \[ vorgenommen\]
</dt> <dd>

Wenn die Funktion fehlschlägt, gibt dieser Parameter an, ob eine Fehlermeldung angezeigt werden soll.

</dd> <dt>

*Protokollieren* \[ in\]
</dt> <dd>

Ein Handle für das Protokoll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt den OC Manager-Kontextwert zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**OCM- \_ Client \_ Rückrufe**](ocm-client-callbacks.md)
</dt> <dt>

[**Okbeenden**](octerminate.md)
</dt> </dl>

 

 

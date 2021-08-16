---
description: Initialisiert den optionalen Komponenten-Manager.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: OcInitialize-Funktion
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
ms.openlocfilehash: 08e7ffd7f8ad6faa2b08f937627627b6e74bbc09505482c589023db5dae37677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826745"
---
# <a name="ocinitialize-function"></a>OcInitialize-Funktion

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

*Rückrufe* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**OCM \_ CLIENT \_ CALLBACKS-Struktur,**](ocm-client-callbacks.md) die die Rückruffunktionen angibt, die vom OC-Manager zum Ausführen verschiedener Aufgaben verwendet werden sollen.

</dd> <dt>

*MasterOcInfName* \[ In\]
</dt> <dd>

Der Pfad der OC-Master-INF-Datei.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.

<dl> <dt>

<span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT \_ FORCENEWINF** (0x00000001)
</dt> <dt>

<span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT \_ KILLSUBCOMPS** (0x00000002)
</dt> <dt>

<span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT \_ RUNQUIET** (0x00000004)
</dt> <dt>

<span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT \_ LANGUAGEAWARE** (0x00000008)
</dt> </dl> </dd> <dt>

*ShowError* \[ out\]
</dt> <dd>

Wenn die Funktion fehlschlägt, gibt dieser Parameter an, ob eine Fehlermeldung angezeigt werden soll.

</dd> <dt>

*Protokollieren* \[ In\]
</dt> <dd>

Ein Handle für das Protokoll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt den Kontextwert des OC-Managers zurück.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_ \_ OCM-CLIENTRÜCKRUFE**](ocm-client-callbacks.md)
</dt> <dt>

[**OcTerminate**](octerminate.md)
</dt> </dl>

 

 

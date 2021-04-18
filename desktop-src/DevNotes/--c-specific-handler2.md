---
description: Wird vom Compiler aufgerufen, um strukturierte Ausnahme Behandlungs Erweiterungen zu implementieren.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: __C_specific_handler-Funktion (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366008"
---
# <a name="__c_specific_handler-function"></a>\_\_C- \_ spezifische \_ Handlerfunktion

Wird vom Compiler aufgerufen, um strukturierte Ausnahme Behandlungs Erweiterungen zu implementieren.

Die relative Adresse des sprachspezifischen Handlers ist in den Informationen zum Entladen enthalten, \_ Wenn Flags UNW- \_ Flag " \_ ehandler" oder "UNW \_ Flag \_ uhandler" festgelegt sind. Der sprachspezifische Handler wird als Teil der Suche nach einem Ausnahmehandler oder als Teil einer Entladung aufgerufen. Weitere Informationen finden Sie unter [sprachspezifischer Handler](/cpp/build/language-specific-handler).

## <a name="syntax"></a>Syntax


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ExceptionRecord* \[ in\]
</dt> <dd>

Stellt einen Zeiger auf einen Ausnahme Daten Satz mit der Win64-Standard Definition bereit.

</dd> <dt>

" *Framesherframe* \[ " in\]
</dt> <dd>

Die Adresse der Basis der fixierten Stapel Zuordnung für diese Funktion.

</dd> <dt>

*ContextRecord* \[ in, out\]
</dt> <dd>

Zeigt auf den Ausnahme Kontext zu dem Zeitpunkt, zu dem die Ausnahme ausgelöst wurde (im Ausnahmehandler), oder im aktuellen "Entlade Kontext" (im Fall eines Beendigungs Handlers).

</dd> <dt>

*DispatcherContext* \[ in, out\]
</dt> <dd>

Verweist auf den Verteiler Kontext für diese Funktion.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>WDM. h</dt> </dl>        |
| Bibliothek<br/> | <dl> <dt>Nzu-nl. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntoskrnl.exe</dt> </dl> |



 


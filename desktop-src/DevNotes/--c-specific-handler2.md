---
description: Wird vom Compiler aufgerufen, um strukturierte Ausnahmebehandlungserweiterungen zu implementieren.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: __C_specific_handler -Funktion (Wdm.h)
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
ms.openlocfilehash: c61d14b591f54ea44ba0f33a36a2ca5acecb129ba46b5f45fcc18185f5d9448c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017828"
---
# <a name="__c_specific_handler-function"></a>\_\_\_C-spezifische \_ Handlerfunktion

Wird vom Compiler aufgerufen, um strukturierte Ausnahmebehandlungserweiterungen zu implementieren.

Die relative Adresse des sprachspezifischen Handlers ist in DEN ENTLADUNGSINFORMATIONEN immer dann vorhanden, wenn \_ flags UNW \_ FLAG \_ EHANDLER oder UNW \_ FLAG \_ UHANDLER festgelegt werden. Der sprachspezifische Handler wird als Teil der Suche nach einem Ausnahmehandler oder als Teil einer Entladung aufgerufen. Weitere Informationen finden Sie unter [Sprachspezifischer Handler.](/cpp/build/language-specific-handler)

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

*ExceptionRecord* \[ In\]
</dt> <dd>

Stellt einen Zeiger auf einen Ausnahmedatensatz mit der Win64-Standarddefinition dar.

</dd> <dt>

*EstablisherFrame* \[ In\]
</dt> <dd>

Die Adresse der Basis der festen Stapelzuordnung für diese Funktion.

</dd> <dt>

*ContextRecord* \[ in, out\]
</dt> <dd>

Verweist auf den Ausnahmekontext zum Zeitpunkt der Ausnahmeausnahme (im Ausnahmehandlerfall) oder auf den aktuellen "Entladungskontext" (im Fall des Beendigungshandlers).

</dd> <dt>

*DispatcherContext* \[ in, out\]
</dt> <dd>

Verweist auf den Verteilerkontext für diese Funktion.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wdm.h</dt> </dl>        |
| Bibliothek<br/> | <dl> <dt>NtosKrnl.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntoskrnl.exe</dt> </dl> |



 


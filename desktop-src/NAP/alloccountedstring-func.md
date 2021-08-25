---
title: AllocCountedString-Funktion (NapUtil.h)
description: Weist Arbeitsspeicher für eine auf NULL terminierte Zeichenfolge zu und gibt ihn in einer CountedString-Struktur zurück.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- AllocCountedString-Funktion NAP
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef205cf7211f25253a3e6ba0cb7cd84ac37dbdb49848b36e844595d632552331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891740"
---
# <a name="alloccountedstring-function"></a>AllocCountedString-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **AllocCountedString-Funktion** reserviert Arbeitsspeicher für eine auf NULL terminierte Zeichenfolge und gibt sie in einer [**CountedString-Struktur**](/windows/win32/api/naptypes/ns-naptypes-countedstring) zurück.

## <a name="syntax"></a>Syntax


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*countedString* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die Adresse einer neu zugeordneten [**CountedString-Struktur.**](/windows/win32/api/naptypes/ns-naptypes-countedstring)

</dd> <dt>

*string* \[ In\]
</dt> <dd>

Ein Zeiger auf die auf NULL beendete Zeichenfolge, die in *countedString zurückgegeben werden soll.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                                   | Beschreibung                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ein ungültiges Argument wurde übergeben.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Das System befindet sich nicht im virtuellen Arbeitsspeicher. Fehler bei diesem Vorgang.<br/> |



 

## <a name="remarks"></a>Hinweise

Alle vom NAP-System unterstützten COM-Schnittstellen verwenden standardmäßige COM-Speicherverwaltungsregeln und die COM-Speicherzuweisungen (**CoTaskMemAlloc** und **CoTaskMemFree**):

-   **In** werden Parameter vom Aufrufer zugeordnet und frei.
-   **Out-Parameter** werden vom Aufrufer zugeordnet und vom Aufrufer mithilfe von **CoTaskMem frei.**
-   **Ein-/Aus-Parameter** werden vom Aufrufer zugeordnet, vom Aufrufer frei und neu zugeordnet und schließlich vom Aufrufer mithilfe von **CoTaskMem frei.**

Alle NAP-Funktionen zum Freien von Arbeitsspeicher geben auch alle eingebetteten Zeiger frei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FreeCountedString**](freecountedstring-func.md)
</dt> </dl>

 

 






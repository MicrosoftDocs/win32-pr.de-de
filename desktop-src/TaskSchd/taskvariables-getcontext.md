---
title: TaskVariables.GetContext-Methode
description: Für die Skripterstellung wird verwendet, um den Kontext zwischen verschiedenen Schritten und Aufgaben in derselben Auftragsinstanz freizugeben.
ms.assetid: c3f1245c-531b-43f4-a3e4-8cb5deedd375
keywords:
- GetContext-Methode Taskplaner
- GetContext-Methode Taskplaner , TaskVariables-Objekt
- TaskVariables-Objekt Taskplaner , GetContext-Methode
topic_type:
- apiref
api_name:
- TaskVariables.GetContext
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c98714d92aba0cffce9d6410ac575c35ec1b7b3e683b954015caebd7719d72b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974700"
---
# <a name="taskvariablesgetcontext-method"></a>TaskVariables.GetContext-Methode

Für die Skripterstellung wird verwendet, um den Kontext zwischen verschiedenen Schritten und Aufgaben in derselben Auftragsinstanz freizugeben. Diese Methode ist nicht implementiert.

## <a name="syntax"></a>Syntax


```VB
TaskVariables.GetContext( _
  ByRef context _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Context (Kontext)* \[ out\]
</dt> <dd>

Der Kontext, der verwendet wird, um den Kontext zwischen verschiedenen Schritten und Aufgaben zu teilen, die sich in derselben Auftragsinstanz befinden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TaskVariables**](taskvariables.md)
</dt> </dl>

 

 






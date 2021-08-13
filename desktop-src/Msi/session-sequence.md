---
description: Die Sequence-Methode des Session-Objekts öffnet eine Abfrage für die angegebene Tabelle, die die Aktionen nach den Zahlen in der Spalte Sequenz sortiert.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Session.Sequence-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 59e9bb09e66ad9a7bff51f1ce2e7e15750749d04a4d2f2c92365b78b29b34585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625118"
---
# <a name="sessionsequence-method"></a>Session.Sequence-Methode

Die **Sequence-Methode** des [**Session-Objekts**](session-object.md) öffnet eine Abfrage für die angegebene Tabelle, die die Aktionen nach den Zahlen in der Spalte Sequenz sortiert. Für jede abgerufene Zeile wird die [**DoAction-Methode**](session-doaction.md) aufgerufen, vorausgesetzt, jeder angegebene Bedingungsausdruck wird nicht als False ausgewertet. Gibt eine Enumeration msiDoActionStatusEnum zurück, wie in der [**DoAction-Methode**](session-doaction.md) beschrieben.

## <a name="syntax"></a>Syntax


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tabelle* 
</dt> <dd>

Erforderlicher Zeichenfolgenname der Tabelle, die für die Sequenzierung verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode wird normalerweise intern von Aktionen der obersten Ebene aufgerufen.

Eine Aktionssequenz, die Aktionen enthält, die das System aktualisieren, z. B. die Aktionen [InstallFiles](installfiles-action.md) und [WriteRegistryValues,](writeregistryvalues-action.md) kann nicht durch Aufrufen der **Sequence-Methode** ausgeführt werden. Eine Ausnahme von dieser Regel besteht darin, dass die **Sequence-Methode** von einer benutzerdefinierten Aktion aufgerufen wird, die in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md) zwischen den Aktionen [InstallInitialize](installinitialize-action.md) und [InstallFinalize](installfinalize-action.md)geplant ist. Aktionen, die das System nicht aktualisieren, z. B. [AppSearch](appsearch-action.md) oder [CostInitialize,](costinitialize-action.md)können aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist als 000C109E-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                             |



 

 





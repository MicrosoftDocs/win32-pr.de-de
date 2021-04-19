---
description: Die Sequence-Methode des Session-Objekts öffnet eine Abfrage für die angegebene Tabelle und ordnet die Aktionen nach den Zahlen in der Sequenz Spalte an.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Session. Sequence-Methode
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
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362135"
---
# <a name="sessionsequence-method"></a>Session. Sequence-Methode

Die **Sequence** -Methode des [**Session**](session-object.md) -Objekts öffnet eine Abfrage für die angegebene Tabelle und ordnet die Aktionen nach den Zahlen in der Sequenz Spalte an. Für jede abgerufene Zeile wird die [**doaction**](session-doaction.md) -Methode aufgerufen, vorausgesetzt, dass ein beliebiger angegebener Bedingungs Ausdruck nicht als false ausgewertet wird. Gibt eine Enumeration msidoaction Status usenum zurück, wie in der [**doaction**](session-doaction.md) -Methode beschrieben.

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

Erforderlicher Zeichen folgen Name der Tabelle, die für die Sequenzierung verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird normalerweise intern von Aktionen der obersten Ebene aufgerufen.

Eine Aktions Sequenz mit Aktionen, die das System aktualisieren, z. b. die Aktionen " [InstallFiles](installfiles-action.md) " und " [schreiteregistryvalues](writeregistryvalues-action.md) ", kann nicht ausgeführt werden, indem die **Sequence** -Methode aufgerufen wird. Eine Ausnahme von dieser Regel ist, wenn die **Sequence** -Methode von einer benutzerdefinierten Aktion aufgerufen wird, die in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) zwischen den [InstallInitialize](installinitialize-action.md) -und [InstallFinalize-Aktionen](installfinalize-action.md)geplant ist. Aktionen, die das System nicht aktualisieren, z. b. [AppSearch](appsearch-action.md) oder [costinitialize](costinitialize-action.md), können aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





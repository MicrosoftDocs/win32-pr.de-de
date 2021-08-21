---
description: Die EvaluateCondition-Methode des Session-Objekts wertet einen logischen Ausdruck aus, der Symbole und Werte enthält. Diese Methode verwendet die MsiEvaluateCondition-Funktion.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Session.EvaluateCondition-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fa5807314092c6245c23a329deb44a644ed54b22640292a06e08a9944f54e4dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629330"
---
# <a name="sessionevaluatecondition-method"></a>Session.EvaluateCondition-Methode

Die **EvaluateCondition-Methode** des [**Session-Objekts**](session-object.md) wertet einen logischen Ausdruck aus, der Symbole und Werte enthält. Diese Methode verwendet die [**MsiEvaluateCondition-Funktion.**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

## <a name="syntax"></a>Syntax


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*condition* 
</dt> <dd>

Erforderliche Zeichenfolge, die den logischen Ausdruck enthält. Weitere Informationen finden Sie unter [Syntax für bedingte Anweisungen.](conditional-statement-syntax.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine ganze Zahl zurück, die die Auswertung der Bedingung angibt.



| Konstante                  | Wert | Beschreibung                               |
|---------------------------|-------|-------------------------------------------|
| msiEvaluateConditionFalse | 0     | Die Bedingung wird als FALSE ausgewertet.         |
| msiEvaluateConditionTrue  | 1     | Die Bedingung wird als true ausgewertet.          |
| msiEvaluateConditionNone  | 2     | Ein bedingter Ausdruck wird nicht bereitgestellt. |
| msiEvaluateConditionError | 3     | Die Bedingung enthält einen Syntaxfehler.    |



 

## <a name="remarks"></a>Hinweise

Bedingte Ausdrücke können verwendet werden, um Feature- und Komponentenzustände zu vergleichen. Die folgende Tabelle zeigt die Feature- und Komponentenzustände, die von der EvaluateCondition-Methode verwendet werden.



| State                 | Wert | Beschreibung                                              |
|-----------------------|-------|----------------------------------------------------------|
| Null                  | Null  | Es wird keine Aktion für das Feature oder die Komponente ergriffen.                 |
| msiInstallStateAbsent | 2     | Das Feature oder die Komponente ist nicht vorhanden.                     |
| msiInstallStateLocal  | 3     | Das Feature oder die Komponente ist auf dem lokalen Computer installiert. |
| msiInstallStateSource | 4     | Das Feature oder die Komponente wird installiert, um von der Quelle aus ausgeführt zu werden.    |



 

> [!Note]  
> Die Zustände werden erst festgelegt, wenn die [**SetInstallLevel-Methode**](session-setinstalllevel.md) entweder direkt oder durch die [CostFinalize-Aktion aufgerufen wird.](costfinalize-action.md) Daher ist die Zustandsüberprüfung nur bei bedingten Ausdrücken in einer Aktionssequenztabelle nützlich.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession ist als \_ 000C109E-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Syntax für bedingte Anweisungen](conditional-statement-syntax.md)
</dt> </dl>

 

 





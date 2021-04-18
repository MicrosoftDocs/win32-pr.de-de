---
description: Die evaluatecondition-Methode des Session-Objekts wertet einen logischen Ausdruck aus, der Symbole und Werte enthält. Diese Methode verwendet die msievaluatecondition-Funktion.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Session. evaluatecondition-Methode
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
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361301"
---
# <a name="sessionevaluatecondition-method"></a>Session. evaluatecondition-Methode

Die **evaluatecondition** -Methode des [**Session**](session-object.md) -Objekts wertet einen logischen Ausdruck aus, der Symbole und Werte enthält. Diese Methode verwendet die [**msievaluatecondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) -Funktion.

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

Erforderliche Zeichenfolge, die den logischen Ausdruck enthält. Weitere Informationen finden Sie unter [bedingte Anweisungs Syntax](conditional-statement-syntax.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine ganze Zahl zurück, die die Auswertung der Bedingung angibt.



| Konstante                  | Wert | BESCHREIBUNG                               |
|---------------------------|-------|-------------------------------------------|
| msievaluateconditionfalse | 0     | Die Bedingung wird zu false ausgewertet.         |
| msievaluateconditiontrue  | 1     | Die Bedingung wird als true ausgewertet.          |
| msievaluateconditionnone  | 2     | Ein bedingter Ausdruck wurde nicht bereitgestellt. |
| msievaluateconditionerror | 3     | Die Bedingung enthält einen Syntax Fehler.    |



 

## <a name="remarks"></a>Bemerkungen

Bedingte Ausdrücke können zum Vergleichen von Funktions-und Komponenten Zuständen verwendet werden. In der folgenden Tabelle sind die Funktions-und Komponenten Zustände aufgeführt, die von der evaluatecondition-Methode verwendet werden.



| State                 | Wert | BESCHREIBUNG                                              |
|-----------------------|-------|----------------------------------------------------------|
| Null                  | Null  | Für das Feature oder die Komponente wurde keine Aktion ausgeführt.                 |
| msiinstallstatemissing | 2     | Die Funktion oder Komponente ist nicht vorhanden.                     |
| msiinstallstatuelocal  | 3     | Die Funktion oder Komponente ist auf dem lokalen Computer installiert. |
| msiinstallstaatource | 4     | Die Funktion oder Komponente wird zum Ausführen von der Quelle installiert.    |



 

> [!Note]  
> Die Zustände werden erst festgelegt, wenn die [**setinstalllevel**](session-setinstalllevel.md) -Methode entweder direkt oder durch die [costfinalize-Aktion](costfinalize-action.md)aufgerufen wird. Daher ist die Zustands Überprüfung nur in bedingtem Ausdruck in einer Aktions Sequenz Tabelle sinnvoll.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Syntax der bedingten Anweisung](conditional-statement-syntax.md)
</dt> </dl>

 

 





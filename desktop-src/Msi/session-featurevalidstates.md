---
description: Die featurevalidstates-Eigenschaft des Session-Objekts gibt eine ganze Zahl zurück, die Bitflags mit jedem relevanten Bit darstellt, das einen gültigen Installations Zustand für das angegebene Feature darstellt.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Session. featurevalidstates (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365706"
---
# <a name="sessionfeaturevalidstates-property"></a>Session. featurevalidstates (Eigenschaft)

Die **featurevalidstates** -Eigenschaft des [**Session**](session-object.md) -Objekts gibt eine ganze Zahl zurück, die Bitflags mit jedem relevanten Bit darstellt, das einen gültigen Installations Zustand für das angegebene Feature darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher Zeichen folgen Name des Funktions Elements, dessen gültige Installations Zustände abgerufen werden sollen.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert besteht wie folgt aus Bitflags. Bit 0: Wenn festgelegt, ist Local ein gültiger Zustand. Bit 1: Wenn festgelegt, ist die Quelle ein gültiger Zustand.

Die **featurevalidstates** -Eigenschaft ist nur erfolgreich, nachdem das Installationsprogramm die Aktionen " [costinitialize](costinitialize-action.md) " und " [costfinalize](costfinalize-action.md) " aufgerufen hat.

**Featurevalidstates** bestimmt die Zustands Gültigkeit, indem alle Komponenten abgefragt werden, die mit der angegebenen Funktion verknüpft sind, ohne den aktuell installierten Zustand einer beliebigen Komponente zu berücksichtigen.

Die möglichen gültigen Zustände für eine Funktion werden wie folgt bestimmt:

-   Wenn die Funktion keine Komponenten enthält, sind sowohl InstallState \_ local als auch InstallState \_ Source gültige Zustände für das Feature.
-   Wenn mindestens eine Komponente der Funktion über das Attribut "msidbcomponentattributeslocalonly" oder "msidbcomponentattributesoptional" verfügt, ist "InstallState \_ local" ein gültiger Status für die Funktion.
-   Wenn mindestens eine Komponente der Funktion über ein Attribut von msidbcomponentattributessourceonly oder msidbcomponentattributesoptionalen verfügt, ist die InstallState- \_ Quelle ein gültiger Status für die Funktion.
-   Wenn eine Datei einer Komponente, die zur Funktion gehört, gepatcht wird oder aus einer komprimierten Quelle entfernt wird, ist die InstallState- \_ Quelle nicht als gültiger Status für das Feature enthalten.
-   Die InstallState-Ankündigung \_ ist kein gültiger Status, wenn die Funktion keine Ankündigung zulässt (msidbfeatureattributesdisallowankündigungs), oder die Funktion erfordert Platt Form Unterstützung für Ankündigungen (msidbfeatureattributesnounsupportedankündigungs Ankündigung), und die Plattform unterstützt diese Funktion nicht.
-   "InstallState \_ Missing" ist ein gültiger Status für die Funktion, wenn die Attribute "msidbfeatureattributesuidisallowmissing" nicht enthalten.
-   Gültige Zustände für untergeordnete Funktionen, die für die übergeordnete Funktion gekennzeichnet sind (msidbfeatureattributesfollowparent), basieren auf der Aktion oder dem installierten Status der übergeordneten Funktion.

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





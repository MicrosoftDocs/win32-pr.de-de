---
description: Die FeatureValidStates-Eigenschaft des Session-Objekts gibt eine ganze Zahl zurück, die Bitflags darstellt, wobei jedes relevante Bit einen gültigen Installationszustand für das angegebene Feature darstellt.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Session.FeatureValidStates-Eigenschaft
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
ms.openlocfilehash: 2c6b7e2683ea9c3e82684f77057319fb359429036cd43192fa9793ff7490386e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629210"
---
# <a name="sessionfeaturevalidstates-property"></a>Session.FeatureValidStates-Eigenschaft

Die **FeatureValidStates-Eigenschaft** des [**Session-Objekts**](session-object.md) gibt eine ganze Zahl zurück, die Bitflags darstellt, wobei jedes relevante Bit einen gültigen Installationszustand für das angegebene Feature darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher Zeichenfolgenname des Featureelements, dessen gültiger Installationszustände abgerufen werden sollen.

## <a name="remarks"></a>Hinweise

Der Rückgabewert besteht wie folgt aus Bitflags. Bit 0: Wenn festgelegt, ist Local ein gültiger Zustand. Bit 1: Wenn festgelegt, ist Source ein gültiger Zustand.

Die **FeatureValidStates-Eigenschaft** ist erst erfolgreich, nachdem das Installationsprogramm die Aktionen [CostInitialize](costinitialize-action.md) und [CostFinalize](costfinalize-action.md) aufgerufen hat.

**FeatureValidStates** bestimmt die Gültigkeit des Zustands, indem alle Komponenten abgefragt werden, die mit dem angegebenen Feature verknüpft sind, ohne den aktuellen installierten Zustand einer Komponente zu berücksichtigen.

Die möglichen gültigen Zustände für ein Feature werden wie folgt bestimmt:

-   Wenn das Feature keine Komponenten enthält, sind sowohl INSTALLSTATE LOCAL als auch \_ INSTALLSTATE \_ SOURCE gültige Status für das Feature.
-   Wenn mindestens eine Komponente des Features über das Attribut msidbComponentAttributesLocalOnly oder msidbComponentAttributesOptional verfügt, ist INSTALLSTATE \_ LOCAL ein gültiger Zustand für das Feature.
-   Wenn mindestens eine Komponente des Features über das Attribut msidbComponentAttributesSourceOnly oder msidbComponentAttributesOptional verfügt, ist INSTALLSTATE \_ SOURCE ein gültiger Zustand für das Feature.
-   Wenn eine Datei einer Komponente, die zum Feature gehört, gepatcht oder aus einer komprimierten Quelle stammt, ist INSTALLSTATE \_ SOURCE nicht als gültiger Zustand für das Feature enthalten.
-   INSTALLSTATE \_ ADVERTISE ist kein gültiger Zustand, wenn das Feature Ankündigungen (msidbFeatureAttributesDisallowAdvertise) nicht zulässt oder die Funktion Plattformunterstützung für Ankündigungen (msidbFeatureAttributesNoUnsupportedAdvertise) erfordert und die Plattform dies nicht unterstützt.
-   INSTALLSTATE \_ ABSENT ist ein gültiger Zustand für das Feature, wenn die Attribute msidbFeatureAttributesUIDisallowAbsent nicht enthalten.
-   Gültige Status für untergeordnete Features, die dem übergeordneten Feature (msidbFeatureAttributesFollowParent) folgen, basieren auf der Aktion oder dem installierten Zustand des übergeordneten Features.

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist als 000C109E-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                             |



 

 





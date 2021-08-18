---
description: Die FeatureRequestState-Eigenschaft ist eine Lese-/Schreibeigenschaft des Session-Objekts.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Session.FeatureRequestState(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c1198f96dde27ec4056ad099f1bb4a3eed591fdd3d390c843cec42af82d4140e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629220"
---
# <a name="sessionfeaturerequeststate-property"></a>Session.FeatureRequestState(Eigenschaft)

Die **FeatureRequestState-Eigenschaft** ist eine Lese-/Schreibeigenschaft des [**Session-Objekts.**](session-object.md) Sie kann verwendet werden, um den aktuellen Aktionsstatus eines Features zu erhalten oder eine Änderung der Aktion eines Features und seiner Unterfeatures an fordern. Das Feature muss in der Tabelle [Feature benannt](feature-table.md) werden. Wenn eine Änderung des Aktionsstatus eines Features angefordert wird, kann auch der Aktionsstatus aller Komponenten des geänderten Features geändert werden. Der Aktionsstatus von Komponenten, die von mehr als einem Feature gemeinsam genutzt werden, wird entsprechend dem neuen Featureaktionsstatus geändert (siehe Hinweise). Die **FeatureRequestState-Eigenschaft** kann auch verwendet werden, um alle Features gleichzeitig zu konfigurieren, indem das Schlüsselwort ALL anstelle eines bestimmten Featurenamens angegeben wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche Zeichenfolge, die den Namen des zu konfigurierenden Features angibt. Um alle Features auf einen gewünschten Anforderungszustand zu setzen, verwenden Sie das reservierte Wort, bei dem die Groß-/Kleinschreibung nicht beachtet wird: ALL.

## <a name="remarks"></a>Hinweise

Die [**SetInstallLevel-Methode**](session-setinstalllevel.md) muss aufgerufen werden, bevor **FeatureRequestState aufgerufen wird.**

Wenn der aktuelle Zustand des Features angefordert wird, gibt die **FeatureRequestState-Eigenschaft** einen der folgenden Werte zurück.



| Name des Auswahlzustands         | Bedeutung                                                               |
|------------------------------|-----------------------------------------------------------------------|
| msiInstallStateUnknown = -1  | Für das Feature wird keine Aktion ergriffen. Dies entspricht NULL.       |
| msiInstallStateAdvertised =1 | Das Feature soll angekündigt werden.                                          |
| msiInstallStateAbsent = 2    | Das Feature muss entfernt werden.                                             |
| msiInstallStateLocal = 3     | Das Feature muss als "run-local" installiert werden.                              |
| msiInstallStateSource = 4    | Das Feature muss als "Run-from-Source" installiert werden.                        |
| msiInstallStateDefault = 5   | Das Feature muss mit dem aktuellen Aktionsstatus des Features neu installiert werden. |



 

Der folgende Befehl erhält beispielsweise den aktuellen Status von "MyFeature" aus einer benutzerdefinierten VBScript-Aktion.


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



Wenn der Zustand des Features konfiguriert wird, sollte die **FeatureRequestState-Eigenschaft** auf einen der folgenden Werte festgelegt werden.



| Name des Auswahlzustands          | Bedeutung                                 |
|-------------------------------|-----------------------------------------|
| msiInstallStateAdvertised = 1 | Geben Sie das Feature an.                  |
| msiInstallStateAbsent = 2     | Entfernen Sie das Feature.                     |
| msiInstallStateLocal = 3      | Installieren Sie das Feature als run-local.       |
| msiInstallStateSource = 4     | Installieren Sie das Feature als "Run-from-Source". |



 

Die folgenden Anforderungen werden beispielsweise von einer benutzerdefinierten VBScript-Aktion ausgeführt, die "MyFeature" installiert, um lokal auf dem Computer ausgeführt zu werden.


```VB
Session.FeatureRequestState("MyFeature")=3
```



Wenn **FeatureRequestState** aufgerufen wird, versucht das Installationsprogramm, den Aktionszustand jeder Komponente, die an das angegebene Feature gebunden ist, so gut wie möglich auf den angegebenen Zustand festzulegen. Es gibt jedoch häufig Situationen, in denen die Anforderung nicht vollständig umgesetzt werden kann. Wenn ein Feature beispielsweise über die [Tabelle FeatureComponents](featurecomponents-table.md) an zwei Komponenten gebunden ist: Komponente A und Komponente B, und Komponente A verfügt über das **Attribut msidbComponentAttributesLocalOnly** und Komponente B über das **Attribut msidbComponentAttributesSourceOnly.** Wenn in diesem Fall **FeatureRequestState** mit dem angeforderten Status msiInstallStateLocal oder msiInstallStateSource aufgerufen wird, kann die Anforderung für beide Komponenten nicht unterstützt werden. In diesem Fall können beide Komponenten aktiviert werden, wenn Komponente A auf msiInstallStateLocal und Komponente B auf msiInstallStateSource festgelegt ist.

Wenn mehrere Features mit einer einzelnen Komponente verknüpft sind, wird der endgültige Aktionsstatus dieser Komponente wie folgt bestimmt: Wenn mindestens ein Feature die lokale Installation der Komponente aufruft, wird msiInstallStateLocal installiert. Wenn mindestens ein Feature die Ausführung der Komponente über das Quellmedium aufruft, wird msiInstallStateSource installiert. Wenn mindestens ein Feature die Entfernung der Komponente erfordert, ist der Aktionsstatus msiInstallStateAbsent. Weitere Informationen dazu, wie Features für die Installation ausgewählt werden, finden Sie in der [Tabelle Feature.](feature-table.md)

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession ist als \_ 000C109E-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sitzungskonsistenz**](session-object.md)
</dt> <dt>

[Feature](feature-table.md)
</dt> </dl>

 

 





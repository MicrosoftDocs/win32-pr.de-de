---
description: Die featurerequeststate-Eigenschaft ist eine Lese-/Schreibeigenschaft des Session-Objekts.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Session. featurerequeststate (Eigenschaft)
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
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368518"
---
# <a name="sessionfeaturerequeststate-property"></a>Session. featurerequeststate (Eigenschaft)

Die **featurerequeststate** -Eigenschaft ist eine Lese-/Schreibeigenschaft des [**Session**](session-object.md) -Objekts. Sie kann verwendet werden, um den aktuellen Aktionszustand eines Features zu erhalten oder eine Änderung der Aktion einer Funktion und ihrer untergeordneten Funktionen anzufordern. Die [Funktion muss](feature-table.md) in der Featuretabelle benannt werden. Wenn eine Änderung des Aktions Zustands eines Features angefordert wird, kann auch der Aktions Status aller Komponenten des geänderten Features geändert werden. Der Aktions Status von Komponenten, die von mehreren Features gemeinsam verwendet werden, wird je nach dem Status der neuen Funktions Aktion entsprechend geändert (siehe Hinweise). Die **featurerequeststate** -Eigenschaft kann auch verwendet werden, um alle Features gleichzeitig zu konfigurieren, indem das Schlüsselwort all anstelle eines bestimmten Featurenamens angegeben wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche Zeichenfolge, die den Namen des zu konfigurierenden Features angibt. Um alle Funktionen auf einen gewünschten Anforderungs Status festzulegen, verwenden Sie die reservierte Groß-/Kleinschreibung nicht.

## <a name="remarks"></a>Bemerkungen

Die [**setinstalllevel**](session-setinstalllevel.md) -Methode muss vor dem Aufruf von **featurerequeststate** aufgerufen werden.

Wenn der aktuelle Status der Funktion angefordert wird, gibt die **featurerequeststate** -Eigenschaft einen der folgenden Werte zurück.



| Name des Auswahl Zustands         | Bedeutung                                                               |
|------------------------------|-----------------------------------------------------------------------|
| msiinstallstateunknown =-1  | Für das Feature wird keine Aktion ausgeführt. Dies entspricht NULL.       |
| msiinstallstateangekündigten = 1 | Das Feature muss angekündigt werden.                                          |
| msiinstallstatemissing = 2    | Das Feature muss entfernt werden.                                             |
| msiinstallstatuelocal = 3     | Das Feature muss als "Run-local" installiert werden.                              |
| msiinstallstaatource = 4    | Das Feature muss als "Run-From-Source" installiert werden.                        |
| msiinstallstatedefault = 5   | Das Feature muss mit dem aktuellen Aktionszustand der Funktion neu installiert werden. |



 

Der folgende Code ruft beispielsweise den aktuellen Status von "myfeature" aus einer benutzerdefinierten VBScript-Aktion ab.


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



Wenn der Status der Funktion konfiguriert wird, sollte die Eigenschaft **featurerequeststate** auf einen der folgenden Werte festgelegt werden.



| Name des Auswahl Zustands          | Bedeutung                                 |
|-------------------------------|-----------------------------------------|
| msiinstallstateangekündigten = 1 | Ankündigen Sie das Feature.                  |
| msiinstallstatemissing = 2     | Entfernen Sie die Funktion.                     |
| msiinstallstatuelocal = 3      | Installieren Sie die Funktion als "Run-local".       |
| msiinstallstaatource = 4     | Installieren Sie die Funktion als "aus Quelle ausführen". |



 

Beispielsweise werden die folgenden Anforderungen aus einer benutzerdefinierten VBScript-Aktion, die "myfeature" für die lokale Installation auf dem Computer installiert ist, installiert.


```VB
Session.FeatureRequestState("MyFeature")=3
```



Wenn **featurerequeststate** aufgerufen wird, versucht das Installationsprogramm, den Aktionszustand für jede Komponente, die an die angegebene Funktion gebunden ist, möglichst am besten in den angegebenen Zustand zu setzen. Es gibt jedoch häufige Situationen, in denen die Anforderung nicht vollständig berücksichtigt werden kann. Wenn z. b. eine Funktion mit zwei Komponenten verknüpft ist, die Komponente a und Komponente b durch die [FeatureComponents](featurecomponents-table.md) -Tabelle und Komponente a das **msidbcomponentattributeslocalonly** -Attribut und Komponente b das **msidbcomponentattributessourceonly** -Attribut. Wenn **featurerequeststate** in diesem Fall mit dem angeforderten Zustand msiinstallstatelocal oder msiinstallstaatource aufgerufen wird, kann die Anforderung für beide Komponenten nicht berücksichtigt werden. In diesem Fall können beide Komponenten eingeschaltet werden, wobei Komponente a auf msiinstallstatelocal und Komponente B auf msiinstallstaatource festgelegt ist.

Wenn mehr als eine Funktion mit einer einzelnen Komponente verknüpft ist, wird der endgültige Aktions Status der Komponente wie folgt bestimmt: Wenn mindestens ein Feature aufruft, dass die Komponente lokal installiert werden soll, wird msiinstallstatelocal installiert. Wenn mindestens ein Feature aufruft, damit die Komponente vom Quell Medium aus ausgeführt wird, wird msiinstallstaatource installiert. Wenn mindestens ein Feature zum Entfernen der Komponente aufruft, lautet der Aktionszustand msiinstallstatemissing. Weitere Informationen zur Auswahl von Features für die Installation finden Sie [in der](feature-table.md) Featuretabelle.

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sitzung**](session-object.md)
</dt> <dt>

[Feature](feature-table.md)
</dt> </dl>

 

 





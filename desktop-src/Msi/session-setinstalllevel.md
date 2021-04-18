---
description: Die setinstalllevel-Methode des Session-Objekts legt die Installations Ebene für die aktuelle Installation auf einen angegebenen Wert fest und berechnet die SELECT-und install-Zustände für alle Features in der Featuretabelle neu.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Session. setinstalllevel-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354810"
---
# <a name="sessionsetinstalllevel-method"></a>Session. setinstalllevel-Methode

Die **setinstalllevel** -Methode des [**Session**](session-object.md) -Objekts legt die Installations Ebene für die aktuelle Installation auf einen angegebenen Wert fest und berechnet die SELECT-und install-Zustände für alle Features in der Featuretabelle neu. Außerdem wird der Aktions Status der einzelnen Komponenten in der [Komponenten Tabelle](component-table.md) basierend auf der neuen Ebene festgelegt.

## <a name="syntax"></a>Syntax


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*installLevel* 
</dt> <dd>

Die angeforderte neue Installations Ebene ist erforderlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [costinitialize-Aktion](costinitialize-action.md) muss vor dem Aufrufen von **setinstalllevel** ausgeführt werden.

Wenn für den Parameter " *INSTALLLEVEL* " der Wert 0 übergeben wird, wird die aktuelle Installations Ebene nicht geändert, aber alle Funktionen werden nach wie vor auf der aktuellen Installations Ebene aktualisiert. Diese Funktion kann z. b. vom Handlermodul verwendet werden, um die gesamte Auswahl an einem beliebigen Punkt im Benutzeroberflächen-Auswahl Vorgang auf Ihre anfänglichen Standardzustände zurückzusetzen.

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





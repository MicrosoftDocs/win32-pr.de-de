---
description: Unabhängige Softwarehersteller (INDEPENDENT Software Vendors, ISVs) können den Satz bekannter Ordner auf einem System erweitern, indem sie eigene bekannte Ordner registrieren.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Erweitern bekannter Ordner mit benutzerdefinierten Ordnern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68a04a5ef10c8e3ee909944e6782cf32ca6aa2aa6b50e03f018f31a6aafe529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350870"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a>Erweitern bekannter Ordner mit benutzerdefinierten Ordnern

Unabhängige Softwarehersteller (INDEPENDENT Software Vendors, ISVs) können den Satz bekannter Ordner auf einem System erweitern, indem sie eigene bekannte Ordner registrieren. Nach der Registrierung sind diese Ordner von Drittanbietern dem System bekannt. Sie werden von jedem Aufruf von [**IKnownFolderManager::GetFolderIds gefunden.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) Beachten Sie, dass ein bekannter Ordner ein Computerordner sein muss. Sie können keinen benutzerspezifischen bekannten Ordner erstellen.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Definieren Sie Ihren bekannten Ordner über eine [**KNOWNFOLDER \_ DEFINITION-Struktur.**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition)

### <a name="step-2"></a>Schritt 2:

Registrieren Sie den bekannten Ordner durch einen Aufruf von [**IKnownFolderManager::RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).

## <a name="remarks"></a>Hinweise

Wenn Sie im Rahmen der Installation einen bekannten Ordner für Ihre Anwendung erstellen, müssen Sie auch [**IKnownFolderManager::UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) als Teil des Deinstallationscodes hinzufügen.

Berücksichtigen Sie, warum Ihr Ordner in das bekannte Ordnersystem aufgenommen werden soll, bevor Sie ihn registrieren. Sie sollten einen gültigen Grund dafür haben, den Ordner auf diese Ebene der Systemsichtbarkeit zu erhöhen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bekannte Ordner (Beispiel)](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 

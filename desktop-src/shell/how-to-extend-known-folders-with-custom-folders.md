---
description: Unabhängige Softwarehersteller (ISVs) können den Satz bekannter Ordner auf einem System erweitern, indem Sie bekannte Ordner eigenständig registrieren.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Erweitern bekannter Ordner mit benutzerdefinierten Ordnern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215942"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a>Erweitern bekannter Ordner mit benutzerdefinierten Ordnern

Unabhängige Softwarehersteller (ISVs) können den Satz bekannter Ordner auf einem System erweitern, indem Sie bekannte Ordner eigenständig registrieren. Nach der Registrierung sind die Ordner von Drittanbietern dem System bekannt. Sie werden durch einen beliebigen Aufrufen von [**iknownfoldermanager:: getfolderids**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids)gefunden. Beachten Sie, dass ein bekannter Ordner ein Ordner pro Computer sein muss. Es ist nicht möglich, einen pro Benutzer bekannten Ordner zu erstellen.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Definieren Sie ihren bekannten Ordner über eine [**knownfolder- \_ Definitions**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) Struktur.

### <a name="step-2"></a>Schritt 2:

Registrieren Sie den bekannten Ordner durch einen [**iknownfoldermanager:: registerfolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder)-Befehl.

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen bekannten Ordner für Ihre Anwendung als Teil des Installationsvorgangs erstellen, müssen Sie auch [**iknownfoldermanager:: unregisterfolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) als Teil Ihres uninstallationscodes einschließen.

Berücksichtigen Sie, warum der Ordner vor der Registrierung in das bekannte Ordnersystem aufgenommen werden soll. Sie sollten einen gültigen Grund haben, den Ordner auf diese Ebene der System Sichtbarkeit zu erhöhen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bekannte Ordner (Beispiel)](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 

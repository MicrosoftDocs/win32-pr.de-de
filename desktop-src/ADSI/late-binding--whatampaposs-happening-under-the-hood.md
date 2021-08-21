---
title: Spätes Binden, was im Kopf passiert
description: In diesem Thema wird beschrieben, wie späte Bindung in ADSI funktioniert.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI , späte Bindung, was im Kopf geschieht
- Binden von AD, späte Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c479472a2974f31e8ecdd4308b01cf7c7251eada3f907d5d90ecf152028399b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637890"
---
# <a name="late-binding-whats-happening-under-the-hood"></a>Späte Bindung: Was geschieht im Kopf?

In der folgenden Liste wird der allgemeine Prozess zum Ausführen einer späteren Bindung beschrieben:

-   Etwas wird an ein ADSI-Verzeichnisobjekt gebunden. Beispielsweise wird "LDAP://CN=Jeffsmith,OU=Sales,DC=Fabrikam,DC=COM" mit der späteren COM-Bindung gebunden. Dies bewirkt, dass ADSI die [**QueryInterface-Methode**](/windows/win32/api/oaidl/nn-oaidl-idispatch) auf der **IDispatch-Schnittstelle** aufruft.
-   ADSI findet ein Objekt in der Benutzerklasse und erstellt ein Objekt, das die entsprechenden Schnittstellen unterstützt, z. B. [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) [**IADsUser.**](/windows/desktop/api/Iads/nn-iads-iadsuser)
-   ADSI führt eine Suche in der Registrierung durch und sucht erweiterungs-CLSIDs für den Benutzer. Beachten Sie, dass ADSI diese Daten zwischenspeichert.
-   Etwas ruft die **MyNewMethod-Methode** auf. ADSI sucht seine Dispatch-ID und die Dispatch-IDs für andere ADSI-Erweiterungen. ADSI sucht dann die Erweiterung, die diesen Aufruf bedient, und ruft die [**IADsExtension-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsextension) für diese Erweiterung auf.
-   Die Erweiterung führt die Funktion aus.
-   Nun ruft der Clientwriter die **YourNewMethod-Methode** mithilfe der [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) für die aktuelle Erweiterung auf. Die **IDispatch-Implementierung** der Erweiterung delegiert zurück an **IDispatch** für ADSI.
-   Der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) für ADSI sucht erneut nach der entsprechenden Erweiterung oder selbst und ruft dann die entsprechende Erweiterung mithilfe der [**IADsExtension-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsextension) für diese Erweiterung auf.

 

 
---
title: Installieren einer EAP-Methode
description: Befolgen Sie die nachfolgenden Anweisungen, um eine vom Benutzer implementierte EAP-Methode auf einem Client Computer mit EAPHost zu installieren.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726288"
---
# <a name="installing-an-eap-method"></a>Installieren einer EAP-Methode

Befolgen Sie die nachfolgenden Anweisungen, um eine vom Benutzer implementierte EAP-Methode auf einem Client Computer mit EAPHost zu installieren.

-   Implementieren Sie [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) für Ihre EAP-Methoden-dll. Mit diesen Funktionen werden die entsprechenden Registrierungsschlüssel für die EAP-Methode während der Installation und des Prozesses (deinstallieren) hinzugefügt und entfernt.

    Informationen zu den spezifischen Registrierungs Schlüsseln, die der Installation einer EAP-Methode zugeordnet sind, finden Sie im Thema [Registrierungs Konfiguration für EAP-Methoden](registry-keys-for-eap-methods.md) .

-   Installieren Sie die dll, die die EAP-Methoden Implementierung enthält, mit dem folgenden Konsolen Befehl.

     *&lt; Name &gt;* derregsvr32.exe-dll

    Verwenden Sie zum Deinstallieren der DLL den folgenden Konsolen Befehl:

    *&lt; Name &gt;* der **regsvr32.exe** **/u** -dll

-   Starten Sie den EAPHost-Dienst neu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> </dl>

 

 
---
title: Installieren einer EAP-Methode
description: Befolgen Sie die anweisungen unten, um eine vom Benutzer implementierte EAP-Methode auf einem Clientcomputer zu installieren, auf dem EAPHost ausgeführt wird.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e047c5a8f0bc4cedcc207016d6f66530b392869839dda128635cd31ac459011a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021580"
---
# <a name="installing-an-eap-method"></a>Installieren einer EAP-Methode

Befolgen Sie die anweisungen unten, um eine vom Benutzer implementierte EAP-Methode auf einem Clientcomputer zu installieren, auf dem EAPHost ausgeführt wird.

-   Implementieren Sie [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) für Ihre EAP-Methoden-DLL. Diese Funktionen fügen während der Installation und (Deinstallation) die entsprechenden Registrierungsschlüssel für Ihre EAP-Methode hinzu und entfernen sie.

    Informationen zu den spezifischen Registrierungsschlüsseln, die der Installation einer EAP-Methode zugeordnet sind, finden Sie im Thema [Registrierungskonfiguration für EAP-Methoden.](registry-keys-for-eap-methods.md)

-   Installieren Sie die DLL, die die Implementierung der EAP-Methode enthält, mit dem folgenden Konsolenbefehl.

    **regsvr32.exe** *&lt; DLL-Name &gt;*

    Verwenden Sie den folgenden Konsolenbefehl, um die DLL zu deinstallieren:

    **regsvr32.exe** *&lt; /u-DLL-Name &gt;* 

-   Starten Sie den EAPHost-Dienst neu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> </dl>

 

 
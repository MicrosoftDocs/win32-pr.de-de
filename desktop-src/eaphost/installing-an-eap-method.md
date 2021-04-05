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
# <a name="installing-an-eap-method"></a><span data-ttu-id="7888b-103">Installieren einer EAP-Methode</span><span class="sxs-lookup"><span data-stu-id="7888b-103">Installing an EAP Method</span></span>

<span data-ttu-id="7888b-104">Befolgen Sie die nachfolgenden Anweisungen, um eine vom Benutzer implementierte EAP-Methode auf einem Client Computer mit EAPHost zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7888b-104">Follow the instructions below to install a user-implemented EAP method on a client computer running EAPHost.</span></span>

-   <span data-ttu-id="7888b-105">Implementieren Sie [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) für Ihre EAP-Methoden-dll.</span><span class="sxs-lookup"><span data-stu-id="7888b-105">Implement [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) for your EAP Method DLL.</span></span> <span data-ttu-id="7888b-106">Mit diesen Funktionen werden die entsprechenden Registrierungsschlüssel für die EAP-Methode während der Installation und des Prozesses (deinstallieren) hinzugefügt und entfernt.</span><span class="sxs-lookup"><span data-stu-id="7888b-106">These functions add and remove the appropriate registry keys for your EAP method during the installation and (uninstallation) process.</span></span>

    <span data-ttu-id="7888b-107">Informationen zu den spezifischen Registrierungs Schlüsseln, die der Installation einer EAP-Methode zugeordnet sind, finden Sie im Thema [Registrierungs Konfiguration für EAP-Methoden](registry-keys-for-eap-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="7888b-107">For information on the specific registry keys associated with the installation of an EAP method, see the [Registry Configuration for EAP Methods](registry-keys-for-eap-methods.md) topic.</span></span>

-   <span data-ttu-id="7888b-108">Installieren Sie die dll, die die EAP-Methoden Implementierung enthält, mit dem folgenden Konsolen Befehl.</span><span class="sxs-lookup"><span data-stu-id="7888b-108">Install the DLL that contains the EAP method implementation with the following console command.</span></span>

    <span data-ttu-id="7888b-109"> *&lt; Name &gt;* derregsvr32.exe-dll</span><span class="sxs-lookup"><span data-stu-id="7888b-109">**regsvr32.exe** *&lt;DLL name&gt;*</span></span>

    <span data-ttu-id="7888b-110">Verwenden Sie zum Deinstallieren der DLL den folgenden Konsolen Befehl:</span><span class="sxs-lookup"><span data-stu-id="7888b-110">To uninstall the DLL, use the following console command:</span></span>

    <span data-ttu-id="7888b-111">*&lt; Name &gt;* der **regsvr32.exe** **/u** -dll</span><span class="sxs-lookup"><span data-stu-id="7888b-111">**regsvr32.exe** **/u** *&lt;DLL name&gt;*</span></span>

-   <span data-ttu-id="7888b-112">Starten Sie den EAPHost-Dienst neu.</span><span class="sxs-lookup"><span data-stu-id="7888b-112">Restart the EAPHost service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7888b-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7888b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7888b-114">Verwenden von EAPHost</span><span class="sxs-lookup"><span data-stu-id="7888b-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 
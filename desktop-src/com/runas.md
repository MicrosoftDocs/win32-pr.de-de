---
title: RunAs
description: Konfiguriert eine Klasse so, dass Sie unter einem bestimmten Benutzerkonto ausgeführt wird, wenn Sie von einem Remote Client aktiviert wird, ohne als Dienst Anwendung geschrieben zu werden.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Runas-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337262"
---
# <a name="runas"></a><span data-ttu-id="582c2-104">RunAs</span><span class="sxs-lookup"><span data-stu-id="582c2-104">RunAs</span></span>

<span data-ttu-id="582c2-105">Konfiguriert eine Klasse so, dass Sie unter einem bestimmten Benutzerkonto ausgeführt wird, wenn Sie von einem Remote Client aktiviert wird, ohne als Dienst Anwendung geschrieben zu werden.</span><span class="sxs-lookup"><span data-stu-id="582c2-105">Configures a class to run under a specific user account when activated by a remote client without being written as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="582c2-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="582c2-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a><span data-ttu-id="582c2-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="582c2-107">Remarks</span></span>

<span data-ttu-id="582c2-108">Der-Wert gibt den Benutzernamen an und muss entweder die Form *username*, den *Domänen ***\\*** Benutzer* Namen oder die Zeichenfolge "Interactive User" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="582c2-108">The value specifies the user name and must be either of the form *UserName*, *Domain ***\\*** UserName* or of the string "Interactive User".</span></span> <span data-ttu-id="582c2-109">Sie können auch die Zeichen folgen "NT Authority \\ LocalService" (für lokaler Dienst) und "NT Authority \\ Network Service" (für Netzwerkdienst) angeben.</span><span class="sxs-lookup"><span data-stu-id="582c2-109">You can also specify the strings "nt authority\\localservice" (for Local Service) and "nt authority\\networkservice" (for Network Service).</span></span> <span data-ttu-id="582c2-110">Sie können auch die Zeichenfolge "NT Authority \\ System" angeben, wenn "{*AppID \_ GUID*}" auf einen com-Server verweist, der bereits gestartet wurde oder über einen Eintrag in der Klassen Tabelle verfügt.</span><span class="sxs-lookup"><span data-stu-id="582c2-110">You can also specify the string "nt authority\\system" when {*AppID\_GUID*} refers to a COM server that is already started or that has an entry in the class table.</span></span> <span data-ttu-id="582c2-111">Allerdings können Sie "NT Authority \\ System" nicht mit einem com-Server verwenden, der noch nicht gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="582c2-111">However, you cannot use "nt authority\\system" with a COM server that is not already started.</span></span> <span data-ttu-id="582c2-112">Das Standard Kennwort für "NT Authority \\ LocalService", "NT Authority \\ Network Service" und "NT Authority \\ System" ist "" (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="582c2-112">The default password for "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system" is "" (empty string).</span></span>

> [!Note]  
> <span data-ttu-id="582c2-113">Ab Windows Vista ist ein leeres Kennwort nicht mehr erforderlich, um die \\ runas-Einstellungen "NT Authority LocalService", "NT Authority \\ Network Service" und "NT Authority \\ System"  zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="582c2-113">As of Windows Vista, an empty password is no longer required to configure the "nt authority\\localservice", "nt authority\\networkservice" and "nt authority\\system" **RunAs** settings.</span></span>

 

<span data-ttu-id="582c2-114">Klassen, die so konfiguriert sind, dass Sie als ein bestimmter Benutzer ausgeführt werden, sind möglicherweise nicht unter einer anderen Identität registriert, sodass Aufrufe von [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) mit dieser CLSID fehlschlagen, es sei denn, der Prozess wurde von com im Auftrag einer tatsächlichen Aktivierungs Anforderung gestartet.</span><span class="sxs-lookup"><span data-stu-id="582c2-114">Classes configured to run as a particular user may not be registered under any other identity, so calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID fail unless the process was launched by COM on behalf of an actual activation request.</span></span>

<span data-ttu-id="582c2-115">Der Benutzername wird aus dem **runas** -Wert unter dem **AppID** -Schlüssel der Klasse entnommen.</span><span class="sxs-lookup"><span data-stu-id="582c2-115">The user-name is taken from the **RunAs** value under the class's **AppID** key.</span></span> <span data-ttu-id="582c2-116">Wenn der Benutzername "interaktiver Benutzer" ist, wird der Server in der Identität des aktuell angemeldeten Benutzers ausgeführt und mit dem interaktiven Desktop verbunden.</span><span class="sxs-lookup"><span data-stu-id="582c2-116">If the user name is "Interactive User", the server is run in the identity of the user currently logged on and is connected to the interactive desktop.</span></span>

<span data-ttu-id="582c2-117">Andernfalls wird das Kennwort aus einem Teil der Registrierung abgerufen, der nur für Administratoren des Computers und für das System verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="582c2-117">Otherwise, the password is retrieved from a portion of the registry that is available only to administrators of the computer and to the system.</span></span> <span data-ttu-id="582c2-118">Der Benutzername und das Kennwort werden dann verwendet, um eine Anmelde Sitzung zu erstellen, in der der Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="582c2-118">The user-name and password are then used to create a logon session in which the server is run.</span></span> <span data-ttu-id="582c2-119">Wenn der Benutzer auf diese Weise gestartet wird, wird er mit einer eigenen Desktop-und Fenster Station ausgeführt, und es werden keine Fenster Handles, die Zwischenablage oder andere Elemente der Benutzeroberfläche mit dem interaktiven Benutzer oder anderen Benutzern, die in anderen Benutzerkonten ausgeführt werden, gemeinsam verwendet.</span><span class="sxs-lookup"><span data-stu-id="582c2-119">When launched in this way, the user runs with its own desktop and window station and does not share window-handles, the clipboard, or other UI elements with the interactive user or other user running in other user accounts.</span></span>

<span data-ttu-id="582c2-120">Zum Festlegen eines Kennworts für eine **runas** -Klasse müssen Sie das im System Verzeichnis installierte Verwaltungs Tool DCOMCNFG verwenden.</span><span class="sxs-lookup"><span data-stu-id="582c2-120">To establish a password for a **RunAs** class, you must use the DCOMCNFG administrative tool installed in the system directory.</span></span>

<span data-ttu-id="582c2-121">Bei von DCOM-Servern verwendeten **runas** -Identitäten muss das in dem Wert angegebene Benutzerkonto über die Berechtigung zum Anmelden als Batch Auftrag verfügen.</span><span class="sxs-lookup"><span data-stu-id="582c2-121">For **RunAs** identities used by DCOM servers, the user account specified in the value must have the rights to log on as a batch job.</span></span> <span data-ttu-id="582c2-122">Dieses Recht kann mithilfe des Verwaltungs Tools für lokale Sicherheitsrichtlinien hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="582c2-122">This right can be added using Local Security Policy administrative tool.</span></span> <span data-ttu-id="582c2-123">Wechseln Sie zu **lokale Richtlinien** , und öffnen Sie **Zuweisung von Benutzerrechten**.</span><span class="sxs-lookup"><span data-stu-id="582c2-123">Go to **Local Policies** and open **User Rights Assignment**.</span></span> <span data-ttu-id="582c2-124">Wählen Sie **als Batch Auftrag anmelden aus**, und fügen Sie das Benutzerkonto hinzu.</span><span class="sxs-lookup"><span data-stu-id="582c2-124">Select **Log on as a batch job**, and add the user account.</span></span>

<span data-ttu-id="582c2-125">Der **runas** -Wert wird nicht für Server verwendet, die für die Ausführung als Dienste konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="582c2-125">The **RunAs** value is not used for servers configured to be run as services.</span></span> <span data-ttu-id="582c2-126">COM-Dienste, die unter einer anderen Identität als "LocalSystem" ausgeführt werden müssen, müssen den entsprechenden Benutzernamen und das Kennwort mithilfe des System Steuerungs Applets der Dienste oder der Dienst Controller Funktionen festlegen.</span><span class="sxs-lookup"><span data-stu-id="582c2-126">COM services that need to run under an identity other than LocalSystem should set the appropriate user name and password using the services control panel applet or the service controller functions.</span></span> <span data-ttu-id="582c2-127">(Weitere Informationen zu diesen Funktionen finden Sie unter [Dienste](/windows/desktop/Services/services).)</span><span class="sxs-lookup"><span data-stu-id="582c2-127">(For more information about these functions, see [Services](/windows/desktop/Services/services).)</span></span>

> [!Note]  
> <span data-ttu-id="582c2-128">Ab Microsoft Windows Server 2003 wird die AppID der Klasse explizit aus den **HKEY- \_ \_ Software Klassen der lokalen Computer- \\ \\ \\ AppID** gelesen, die im Gegensatz zu den meisten Registrierungs Schlüsseln nicht mit der Stamm- **\_ \_ \\ AppID der HKEY-Klassen** austauschbar ist.</span><span class="sxs-lookup"><span data-stu-id="582c2-128">As of Microsoft Windows Server 2003, the class AppID is explicitly read from **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\AppID**, which, unlike most registry keys, is not interchangeable with **HKEY\_CLASSES\_ROOT\\AppID**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="582c2-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="582c2-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="582c2-130">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="582c2-130">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 
---
title: Erstellen und Verwalten eines Dienst Verbindungs Punkts
description: Beachten Sie beim Veröffentlichen mit einem SCP, dass Sie aktuelle Daten über die Dienst Instanz enthalten muss.
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- Erstellen und Verwalten eines Dienst Verbindungspunkt-AD
- Dienst Verbindungspunkt AD, erstellen und verwalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038779"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a><span data-ttu-id="f95b9-105">Erstellen und Verwalten eines Dienst Verbindungs Punkts</span><span class="sxs-lookup"><span data-stu-id="f95b9-105">Creating and Maintaining a Service Connection Point</span></span>

<span data-ttu-id="f95b9-106">Beachten Sie beim Veröffentlichen mit einem SCP, dass Sie aktuelle Daten über die Dienst Instanz enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="f95b9-106">When publishing with an SCP, remember that it must contain current data about the service instance.</span></span> <span data-ttu-id="f95b9-107">Andernfalls werden von Clients, die an den Dienst Verbindungs Dienst gebunden sind, veraltete Daten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f95b9-107">Otherwise, clients that bind to the SCP retrieve outdated data.</span></span> <span data-ttu-id="f95b9-108">Das Dienst Installationsprogramm, das einen SCP erstellt, gibt die Anfangswerte für die SCPS-Attribute an.</span><span class="sxs-lookup"><span data-stu-id="f95b9-108">Your service installer, that creates an SCP, specifies the initial values for the SCPs attributes.</span></span> <span data-ttu-id="f95b9-109">Wenn die Dienst Instanz dann gestartet wird, muss Sie den SCP suchen und die Attributwerte ggf. aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f95b9-109">Then, when the service instance starts, it must locate the SCP and update the attribute values, if necessary.</span></span> <span data-ttu-id="f95b9-110">Auf diese Weise werden Clients die aktuellsten Daten sichergestellt.</span><span class="sxs-lookup"><span data-stu-id="f95b9-110">In this way, clients are assured the most current data.</span></span>

<span data-ttu-id="f95b9-111">Nach dem Erstellen des Dienst Verbindungs dienstaners führt Ihr Dienst Installationsprogramm zwei zusätzliche Schritte aus, mit denen der Dienst den SCP aktualisieren kann:</span><span class="sxs-lookup"><span data-stu-id="f95b9-111">After creating the SCP, your service installer performs two additional steps that enable your service to update the SCP:</span></span>

-   <span data-ttu-id="f95b9-112">Legen Sie ACEs in der Sicherheits Beschreibung des SCP-Objekts fest, damit der Dienst SCP-Attribute zur Laufzeit ändern kann.</span><span class="sxs-lookup"><span data-stu-id="f95b9-112">Set ACEs in the security descriptor of the SCP object to enable the service to modify SCP attributes at run time.</span></span> <span data-ttu-id="f95b9-113">Weitere Informationen und ein Codebeispiel finden Sie unter [Aktivieren des Dienst Kontos für den Zugriff auf SCP-Eigenschaften](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f95b9-113">For more information and a code example, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>
-   <span data-ttu-id="f95b9-114">Speichern Sie die **objectGUID** des Dienst Verbindungs Diensts in der Registrierung auf dem Dienst Host Computer.</span><span class="sxs-lookup"><span data-stu-id="f95b9-114">Cache the **objectGUID** of the SCP in the registry on the service host computer.</span></span> <span data-ttu-id="f95b9-115">Der Dienst ruft die zwischengespeicherte GUID zum Binden an den Dienst Verbindungspunkt ab, um die zugehörigen Attribute zu überprüfen und zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f95b9-115">The service retrieves the cached GUID to bind to the SCP to verify and update its attributes.</span></span>

<span data-ttu-id="f95b9-116">Das Dienst Installationsprogramm speichert die **objectGUID** des SCP-dienstanders und nicht seinen DN.</span><span class="sxs-lookup"><span data-stu-id="f95b9-116">The service installer caches the SCP's **objectGUID** rather than its DN.</span></span> <span data-ttu-id="f95b9-117">Die **objectGUID** ändert sich nie, unabhängig davon, ob der Dienst Verbindungspunkt verschoben oder umbenannt wurde.</span><span class="sxs-lookup"><span data-stu-id="f95b9-117">The **objectGUID** never changes, regardless of whether the SCP is moved or renamed.</span></span> <span data-ttu-id="f95b9-118">Der DN kann sich ändern, wenn ein Administrator den Dienst Verbindungspunkt verschiebt oder umbenennt.</span><span class="sxs-lookup"><span data-stu-id="f95b9-118">The DN can change if an administrator moves or renames the SCP.</span></span> <span data-ttu-id="f95b9-119">Wenn Sie z. b. einen SCP als untergeordnetes Element eines Computer Objekts erstellen, ändert sich der Distinguished Name des Dienst Verbindungs Punkts, wenn der Computer umbenannt oder in eine andere Domäne oder Organisationseinheit verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="f95b9-119">For example, if you create an SCP as a child of a computer object, the distinguished name of the SCP changes if the computer is renamed or moved to a different domain or organizational unit.</span></span>

<span data-ttu-id="f95b9-120">Wenn ein Dienst Installationsprogramm einen SCP erstellt, muss er die **objectGUID** des neu erstellten Objekts lesen und in der Registrierung des Dienst Host Computers Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="f95b9-120">When a service installer creates an SCP, it must read the **objectGUID** of the newly created object and cache it in the registry of the service host computer.</span></span> <span data-ttu-id="f95b9-121">Verwenden Sie die [**IADs:: get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) -Methode, um den **objectGUID** -Wert im Zeichen folgen Format abzurufen, das für die Bindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f95b9-121">Use the [**IADs::get\_GUID**](/windows/desktop/ADSI/iads-property-methods) method to get the **objectGUID** value in string format suitable for binding.</span></span> <span data-ttu-id="f95b9-122">Speichern Sie die GUID-Zeichenfolge als Wert unter dem folgenden Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="f95b9-122">Cache the GUID string as a value under the following registry key.</span></span>

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

<span data-ttu-id="f95b9-123">Dabei ermitteln "Herstellername" und "Produktname" den Hersteller und das Produkt.</span><span class="sxs-lookup"><span data-stu-id="f95b9-123">Where "vendor name" and "product name" identify the vendor and product.</span></span>

<span data-ttu-id="f95b9-124">Wenn der Dienst gestartet wird, ruft er die zwischengespeicherte GUID-Zeichenfolge aus der Registrierung ab und verwendet diese für die Bindung an den SCP.</span><span class="sxs-lookup"><span data-stu-id="f95b9-124">When the service starts, it retrieves the cached GUID string from the registry and uses it to bind to the SCP.</span></span> <span data-ttu-id="f95b9-125">Der Dienst liest die wichtigen SCP-Attribute und vergleicht sie mit den aktuellen Werten.</span><span class="sxs-lookup"><span data-stu-id="f95b9-125">The service reads the important SCP attributes and compares them to current values.</span></span> <span data-ttu-id="f95b9-126">Wenn die SCP-Werte veraltet sind, aktualisiert der Dienst Sie.</span><span class="sxs-lookup"><span data-stu-id="f95b9-126">If the SCP values are outdated, the service updates them.</span></span> <span data-ttu-id="f95b9-127">Zum Aktualisieren von include- **Schlüsselwörtern**, **serviceBindingInformation**, **servicednsname** und **serviceDNSNameType** sind Werte, die der Dienst möglicherweise benötigt.</span><span class="sxs-lookup"><span data-stu-id="f95b9-127">Values that the service might require to update include **keywords**, **serviceBindingInformation**, **serviceDNSName**, and **serviceDNSNameType**.</span></span>

## <a name="examples"></a><span data-ttu-id="f95b9-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f95b9-128">Examples</span></span>

-   [<span data-ttu-id="f95b9-129">Skript Beispiele</span><span class="sxs-lookup"><span data-stu-id="f95b9-129">Script samples</span></span>](script-samples-for-managing-service-connection-points.md)
-   [<span data-ttu-id="f95b9-130">Code Beispiele (C/C++)</span><span class="sxs-lookup"><span data-stu-id="f95b9-130">Code (C/C++) samples</span></span>](code-samples-for-managing-service-connection-points.md)

 

 
---
title: Versions unabhängiger ProgID-Schlüssel
description: Ordnet eine ProgID einer CLSID zu. Dieser Schlüssel wird verwendet, um die neueste Version einer Objekt Anwendung zu bestimmen.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474910"
---
# <a name="version-independent-progid-key"></a><span data-ttu-id="93afe-104">Versions unabhängiger ProgID-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="93afe-104">version-independent ProgID Key</span></span>

<span data-ttu-id="93afe-105">Ordnet eine ProgID einer CLSID zu.</span><span class="sxs-lookup"><span data-stu-id="93afe-105">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="93afe-106">Dieser Schlüssel wird verwendet, um die neueste Version einer Objekt Anwendung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="93afe-106">This key is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="93afe-107">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="93afe-107">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a><span data-ttu-id="93afe-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93afe-108">Remarks</span></span>

<span data-ttu-id="93afe-109">Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="93afe-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

<span data-ttu-id="93afe-110">Das Format für <*Versions unabhängige ProgID*> ist <*Programm*>. <*Komponenten*>, getrennt durch Punkte, keine Leerzeichen und keine Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="93afe-110">The format for <*version-independent ProgID*> is <*program*>.<*component*>, separated by periods, no spaces, and no version number.</span></span> <span data-ttu-id="93afe-111">Die Versions unabhängige ProgID, wie z. b. die ProgID, kann mit einem lesbaren Namen registriert werden.</span><span class="sxs-lookup"><span data-stu-id="93afe-111">The version-independent ProgID, like the ProgID, can be registered with a human-readable name.</span></span>

<span data-ttu-id="93afe-112">*ProgID* ist die ProgID der neuesten installierten Version der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="93afe-112">*ProgID* is the ProgID of the latest installed version of the class.</span></span>

<span data-ttu-id="93afe-113">Anwendungen müssen einen Versions unabhängigen programmatischen Bezeichner unter dem *Versions unabhängigen ProgID-* Schlüssel registrieren.</span><span class="sxs-lookup"><span data-stu-id="93afe-113">Applications must register a version-independent programmatic identifier under the *version-independent ProgID* key.</span></span> <span data-ttu-id="93afe-114">Die Versions unabhängige ProgID bezieht sich auf die-Klasse der Anwendung und ändert sich nicht von Version zu Version, sondern bleibt für alle Versionen von Microsoft Word unverändert.</span><span class="sxs-lookup"><span data-stu-id="93afe-114">The version-independent ProgID refers to the application's class and does not change from version to version, instead remaining constant across all versionsâ€”for example, Microsoft Word Document.</span></span> <span data-ttu-id="93afe-115">Sie wird mit Makro Sprachen verwendet und verweist auf die aktuell installierte Version der-Klasse der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="93afe-115">It is used with macro languages and refers to the currently installed version of the application's class.</span></span> <span data-ttu-id="93afe-116">Die Versions unabhängige ProgID muss mit dem Namen der aktuellen Version der Objekt Anwendung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="93afe-116">The version-independent ProgID must correspond to the name of the latest version of the object application.</span></span>

<span data-ttu-id="93afe-117">Beispielsweise wird die Versions unabhängige ProgID verwendet, wenn eine Containeranwendung ein Diagramm oder eine Tabelle mit einer Symbolleisten Schaltfläche erstellt.</span><span class="sxs-lookup"><span data-stu-id="93afe-117">For example, the version-independent ProgID is used when a container application creates a chart or table with a toolbar button.</span></span> <span data-ttu-id="93afe-118">In dieser Situation kann die Anwendung die Versions unabhängige ProgID verwenden, um die neueste Version der benötigten Objekt Anwendung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="93afe-118">In this situation, the application can use the version-independent ProgID to determine the latest version of the needed object application.</span></span>

<span data-ttu-id="93afe-119">Die Versions unabhängige ProgID wird nur durch den Anwendungscode gespeichert und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="93afe-119">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="93afe-120">Wenn die Versions unabhängige ProgID angegeben ist, gibt die [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) -Funktion die CLSID der aktuellen Version zurück.</span><span class="sxs-lookup"><span data-stu-id="93afe-120">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="93afe-121">Sie können [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) und [**progidfromclsid**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) verwenden, um zwischen diesen beiden Darstellungen zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="93afe-121">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

<span data-ttu-id="93afe-122">Sie können [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) oder [**olereggetusertype**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) verwenden, um den Bezeichner in eine anzeigbare Zeichenfolge zu ändern.</span><span class="sxs-lookup"><span data-stu-id="93afe-122">You can use [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) or [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) to change the identifier to a displayable string.</span></span>

<span data-ttu-id="93afe-123">Wenn kein benutzerdefinierter Handler verwendet wird, sollte der Eintrag auf OLE32.DLL festgelegt werden, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="93afe-123">If a custom handler is not used, the entry should be set to OLE32.DLL, as shown in the following example:</span></span>

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a><span data-ttu-id="93afe-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="93afe-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93afe-125">**CLSIDFromProgID**</span><span class="sxs-lookup"><span data-stu-id="93afe-125">**CLSIDFromProgID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[<span data-ttu-id="93afe-126">**Progidfromclsid**</span><span class="sxs-lookup"><span data-stu-id="93afe-126">**ProgIDFromCLSID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<span data-ttu-id="93afe-127"><ProgID> Wichtigen</span><span class="sxs-lookup"><span data-stu-id="93afe-127"><ProgID> Key</span></span>](-progid--key.md)
</dt> </dl>

 

 





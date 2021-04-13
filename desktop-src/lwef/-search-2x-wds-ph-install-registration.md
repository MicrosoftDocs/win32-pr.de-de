---
title: Installieren und Registrieren von Protokoll Handlern (Features der Legacy-Windows-Umgebung)
description: Das Installieren von Protokoll Handlern umfasst das Kopieren der dll (s) an einen geeigneten Speicherort im Verzeichnis "Programme" und deren Registrierung.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec07f96a92b04fb489aeeb76b705efb81b5754f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340267"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a><span data-ttu-id="c8aa8-103">Installieren und Registrieren von Protokoll Handlern (Features der Legacy-Windows-Umgebung)</span><span class="sxs-lookup"><span data-stu-id="c8aa8-103">Installing and Registering Protocol Handlers (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="c8aa8-104">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c8aa8-105">Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="c8aa8-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="c8aa8-106">Das Installieren von **Protokoll Handlern** umfasst das Kopieren der dll (s) an einen geeigneten Speicherort im Verzeichnis "Programme" und deren Registrierung.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-106">Installing **protocol handlers** involves copying the DLL(s) to an appropriate location in the Program Files directory and registering them.</span></span>

<span data-ttu-id="c8aa8-107">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c8aa8-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="c8aa8-108">Installationsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="c8aa8-108">Installation Guidelines</span></span>](#installation-guidelines)
-   [<span data-ttu-id="c8aa8-109">So registrieren Sie Protokollhandler</span><span class="sxs-lookup"><span data-stu-id="c8aa8-109">To Register Protocol Handlers</span></span>](#to-register-protocol-handlers)
-   [<span data-ttu-id="c8aa8-110">So registrieren Sie Shellerweiterungen</span><span class="sxs-lookup"><span data-stu-id="c8aa8-110">To Register Shell Extensions</span></span>](#to-register-shell-extensions)

## <a name="installation-guidelines"></a><span data-ttu-id="c8aa8-111">Installationsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="c8aa8-111">Installation Guidelines</span></span>

<span data-ttu-id="c8aa8-112">Protokollhandler sollten die Selbstregistrierung für die Installation implementieren und die folgenden Richtlinien befolgen:</span><span class="sxs-lookup"><span data-stu-id="c8aa8-112">Protocol handlers should implement self-registration for installation and should follow these guidelines:</span></span>

-   <span data-ttu-id="c8aa8-113">Das Installationsprogramm muss entweder exe oder das MSI-Installationsprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-113">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="c8aa8-114">Anmerkungen zu dieser Version müssen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-114">Release notes must be provided.</span></span>
-   <span data-ttu-id="c8aa8-115">Ein Eintrag zum **Hinzufügen/Entfernen von Programmen** muss für jedes installierte Add-in erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-115">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="c8aa8-116">Das Installationsprogramm muss alle Registrierungs Einstellungen für einen bestimmten Dateityp oder-Speicher übernehmen, den das aktuelle Add-in versteht.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-116">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="c8aa8-117">Wenn ein vorheriges Add-in überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-117">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="c8aa8-118">Wenn das vorherige Add-in von einem neueren Add-in überschrieben wurde, sollte es möglich sein, die vorherige Add-in-Funktionalität wiederherzustellen und das Standard-Add-in für diesen Dateityp erneut zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-118">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>

## <a name="to-register-protocol-handlers"></a><span data-ttu-id="c8aa8-119">So registrieren Sie Protokollhandler</span><span class="sxs-lookup"><span data-stu-id="c8aa8-119">To Register Protocol Handlers</span></span>

<span data-ttu-id="c8aa8-120">Sie müssen 14 Einträge in der Registrierung vornehmen, um die Protokollhandlerkomponente zu registrieren, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="c8aa8-120">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="c8aa8-121">*Ver \_ IND \_ ProgID* ist die Versions unabhängige ProgID der protokollhandlerimplementierung.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-121">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="c8aa8-122">*Ver \_ DEP \_ ProgID* ist die Versions abhängige ProgID der protokollhandlerimplementierung.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-122">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="c8aa8-123">*CLSID \_ 1* ist die CLSID der protokollhandlerimplementierung.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-123">*CLSID\_1* is the CLSID of the protocol handler implementation</span></span>

1.  <span data-ttu-id="c8aa8-124">Registrieren Sie die Versions unabhängige ProgID mit den folgenden Schlüsseln und Werten:</span><span class="sxs-lookup"><span data-stu-id="c8aa8-124">Register the version independent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CurVer
       (Default) = <Ver_Dep_ProgID>
    ```

2.  <span data-ttu-id="c8aa8-125">Registrieren Sie die Versions abhängige ProgID mit den folgenden Schlüsseln und Werten:</span><span class="sxs-lookup"><span data-stu-id="c8aa8-125">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="c8aa8-126">Registrieren Sie die CLSID des Protokoll Handlers mit den folgenden Schlüsseln und Werten:</span><span class="sxs-lookup"><span data-stu-id="c8aa8-126">Register the protocol handler's CLSID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/InprocServer32
       (Default) = <DLL Install Path>
       Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ProgID
       (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ShellFolder
       Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/TypeLib
       (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/VersionIndependentProgID
       (Default) = <Ver_Ind_ProgID>"
    ```

4.  <span data-ttu-id="c8aa8-127">Registrieren Sie den Protokollhandler bei der Windows-Desktop Suche:</span><span class="sxs-lookup"><span data-stu-id="c8aa8-127">Register the protocol handler with Windows Desktop Search:</span></span>

    ```
    HKEY_LOCAL_MACHINE\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\Windows Desktop Search\DS\Index\ProtocolHandlers\<Protocol Name>
       HasRequirements = dword:00000000
       HasStartPage = dword:00000000
    ```

## <a name="to-register-shell-extensions"></a><span data-ttu-id="c8aa8-128">So registrieren Sie Shellerweiterungen</span><span class="sxs-lookup"><span data-stu-id="c8aa8-128">To Register Shell Extensions</span></span>

<span data-ttu-id="c8aa8-129">Sie müssen zwei Einträge in der Registrierung vornehmen, um die Shellerweiterung des Protokoll Handlers zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c8aa8-129">You need to make two entries in the registry to register the protocol handler's Shell extension.</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 





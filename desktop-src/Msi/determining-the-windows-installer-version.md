---
description: 'Sie können die folgenden Methoden verwenden, um die Windows Installer Version zu bestimmen:'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: Bestimmen der Windows Installer Version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a48434fe415084a93158fb3445a36906d8b8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359142"
---
# <a name="determining-the-windows-installer-version"></a><span data-ttu-id="75f1a-103">Bestimmen der Windows Installer Version</span><span class="sxs-lookup"><span data-stu-id="75f1a-103">Determining the Windows Installer Version</span></span>

<span data-ttu-id="75f1a-104">Sie können die folgenden Methoden verwenden, um die Windows Installer Version zu bestimmen:</span><span class="sxs-lookup"><span data-stu-id="75f1a-104">You can use the following methods to determine the Windows Installer version:</span></span>

-   <span data-ttu-id="75f1a-105">Aufrufen der [**msigetfileversion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) -Funktion, wobei der *szFilePath* -Parameter auf den Pfad der Datei Msi.dll festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="75f1a-105">Call the [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) function with the *szFilePath* parameter set to the path to the file Msi.dll.</span></span>

    <span data-ttu-id="75f1a-106">Sie können die [**shgetknownfolderpath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) -Funktion mit der **CSIDL- \_ System** Konstante aufrufen, um den Pfad zu Msi.dll abzurufen.</span><span class="sxs-lookup"><span data-stu-id="75f1a-106">You can call the [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function with the **CSIDL\_SYSTEM** constant to get the path to Msi.dll.</span></span> <span data-ttu-id="75f1a-107">Ab Windows Vista sollten Anwendungen die [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) -Funktion und das **ref KNOWNFOLDERID** -System verwenden.</span><span class="sxs-lookup"><span data-stu-id="75f1a-107">Beginning with Windows Vista, applications should use the [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) function and the **REFKNOWNFOLDERID** "System."</span></span> <span data-ttu-id="75f1a-108">Vorhandene Anwendungen, die die **SHGetFolderPath** -Funktion und den **CSIDL** -Typ verwenden, funktionieren weiterhin.</span><span class="sxs-lookup"><span data-stu-id="75f1a-108">Existing applications that use the **SHGetFolderPath** function and the **CSIDL** type will continue to work.</span></span>

-   <span data-ttu-id="75f1a-109">Der Wert der Eigenschaft " [**Installer. Version**](installer-version.md) " des [**Installerobjekts**](installer-object.md) entspricht den vier Feld Zeichenfolgen, die in den [veröffentlichten Versionen Windows Installer](released-versions-of-windows-installer.md) Themas aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="75f1a-109">The value of the [**Installer.Version**](installer-version.md) property of the [**Installer Object**](installer-object.md) is equivalent to the four-field strings listed in the [Released Versions of Windows Installer](released-versions-of-windows-installer.md) topic.</span></span>
-   <span data-ttu-id="75f1a-110">Anwendungen können die Windows Installer Version mithilfe von [**dllgetversion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc)erhalten.</span><span class="sxs-lookup"><span data-stu-id="75f1a-110">Applications can get the Windows Installer version by using [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span></span>
-   <span data-ttu-id="75f1a-111">Der Installer legt die [**versionmsi**](versionmsi.md) -Eigenschaft auf die Version von Windows Installer fest, die während der Installation ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75f1a-111">The installer sets the [**VersionMsi**](versionmsi.md) property to the version of Windows Installer that is run during the installation.</span></span>

<span data-ttu-id="75f1a-112">Weitere Informationen finden Sie unter [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="75f1a-112">For more information, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

 

 

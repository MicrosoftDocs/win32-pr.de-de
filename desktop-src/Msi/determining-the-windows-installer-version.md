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
# <a name="determining-the-windows-installer-version"></a>Bestimmen der Windows Installer Version

Sie können die folgenden Methoden verwenden, um die Windows Installer Version zu bestimmen:

-   Aufrufen der [**msigetfileversion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) -Funktion, wobei der *szFilePath* -Parameter auf den Pfad der Datei Msi.dll festgelegt ist.

    Sie können die [**shgetknownfolderpath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) -Funktion mit der **CSIDL- \_ System** Konstante aufrufen, um den Pfad zu Msi.dll abzurufen. Ab Windows Vista sollten Anwendungen die [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) -Funktion und das **ref KNOWNFOLDERID** -System verwenden. Vorhandene Anwendungen, die die **SHGetFolderPath** -Funktion und den **CSIDL** -Typ verwenden, funktionieren weiterhin.

-   Der Wert der Eigenschaft " [**Installer. Version**](installer-version.md) " des [**Installerobjekts**](installer-object.md) entspricht den vier Feld Zeichenfolgen, die in den [veröffentlichten Versionen Windows Installer](released-versions-of-windows-installer.md) Themas aufgeführt sind.
-   Anwendungen können die Windows Installer Version mithilfe von [**dllgetversion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc)erhalten.
-   Der Installer legt die [**versionmsi**](versionmsi.md) -Eigenschaft auf die Version von Windows Installer fest, die während der Installation ausgeführt wird.

Weitere Informationen finden Sie unter [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md).

 

 

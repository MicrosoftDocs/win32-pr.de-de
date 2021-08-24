---
description: 'Sie können die folgenden Methoden verwenden, um die Windows Installer-Version zu bestimmen:'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: Bestimmen der Windows Installerversion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e13907790585356fa4a5bc8376fe87f30793e0e3af71e1b0c113f30cf04b8f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764220"
---
# <a name="determining-the-windows-installer-version"></a>Bestimmen der Windows Installerversion

Sie können die folgenden Methoden verwenden, um die Windows Installer-Version zu bestimmen:

-   Rufen Sie die [**MsiGetFileVersion-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) auf, bei der *der szFilePath-Parameter* auf den Pfad zur Datei Msi.dll.

    Sie können die [**SHGetKnownFolderPath-Funktion**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) mit der **CSIDL \_ SYSTEM-Konstante** aufrufen, um den Pfad zum Msi.dll. Ab Windows Vista sollten Anwendungen die [**SHGetFolderPath-Funktion**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) und die **REFKNOWNFOLDERID** "System" verwenden. Vorhandene Anwendungen, die die **SHGetFolderPath-Funktion** und den **CSIDL-Typ** verwenden, funktionieren weiterhin.

-   Der Wert der [**Installer.Version-Eigenschaft**](installer-version.md) des [**Installer-Objekts**](installer-object.md) entspricht den Zeichenfolgen mit vier Zeichenfolgen, die im Thema Veröffentlichte Versionen von Windows [Installer aufgeführt](released-versions-of-windows-installer.md) sind.
-   Anwendungen können die version Windows Installer mithilfe von [**DllGetVersion erhalten.**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc)
-   Das Installationsprogramm legt die [**VersionMsi-Eigenschaft**](versionmsi.md) auf die Version Windows Installer fest, die während der Installation ausgeführt wird.

Weitere Informationen finden Sie unter [Veröffentlichte Versionen des Windows Installers.](released-versions-of-windows-installer.md)

 

 

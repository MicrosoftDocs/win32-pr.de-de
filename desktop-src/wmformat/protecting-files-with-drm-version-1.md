---
title: Schützen von Dateien mit DRM-Version 1
description: Schützen von Dateien mit DRM-Version 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows Media-Format-SDK, erstellen geschützter Dateien
- Windows Media-Format-SDK, geschützte Dateien
- Advanced Systems Format (ASF), erstellen geschützter Dateien
- ASF (Advanced Systems Format), erstellen geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Advanced Systems Format (ASF), wmstubdrm. lib
- ASF (Advanced Systems Format), wmstubdrm. lib
- Wmstubdrm. lib, erstellen geschützter Dateien
- Wmstubdrm. lib, geschützte Dateien
- Digital Rights Management (DRM), wmstubdrm. lib
- DRM (Digital Rights Management), wmstubdrm. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314518"
---
# <a name="protecting-files-with-drm-version-1"></a>Schützen von Dateien mit DRM-Version 1

Wenn diese Art von Schutz angewendet wird, wird eine DRM-Lizenz der Version 1 generiert, die nur auf dem Computer gültig ist, von dem aus die Lizenz Anforderung stammt. Da kein Schlüssel-oder Schlüssel-Seed festgelegt ist, gibt es keine Möglichkeit, Portable Lizenzen für Inhalte zu generieren, die mit dieser Technik geschützt werden. Wenn Sie jedoch das Windows Media-Format SDK 7,1 oder höher verwenden, können die Lizenzen im Microsoft-Lizenz Migrationsdienst wieder hergestellt werden.

Führen Sie die folgenden Schritte aus, um die DRM-Dateien mit DRM-Version 1 zu schützen:

1.  Verknüpfen Sie die Datei wmstubdrm. lib mit Ihrem Projekt, und aufheben Sie ggf. die Verknüpfung von Wmvcore. lib.
2.  Rufen Sie die [**wmkreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) -Funktion auf, um den Writer zu erstellen. Das erste Argument ist reserviert und muss auf **null** festgelegt werden.
3.  Legen Sie ein Profil fest, das der Writer verwenden soll, indem Sie [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) oder [**iwmwriter:: setprofilebyid**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)aufrufen. Sie müssen ein Profil im Writer festlegen, bevor Sie DRM-Attribute festlegen. DRM wird nur für Profile unterstützt, die die Windows Media Audio oder Windows Media Video Codecs verwenden.
4.  Legen Sie mithilfe der [**iwmheaderinfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) -Methode die folgenden DRM-Eigenschaften fest. Die **Eigenschaft \_ DRM verwenden** weist die DRM-Komponenten an, den Inhalt mithilfe der DRM-Version 1 zu schützen. Die Eigenschaft **DRM- \_ Flags** gibt die Rechte an, die in die lokale Lizenz eingeschlossen werden sollen, die für den Inhalt erstellt wird. Der Wert der **DRM- \_ Ebene** wird auch in der Lizenz gespeichert. er gibt die minimale Ebene an, die für den Zugriff auf den Inhalt erforderlich ist. 150 ist die empfohlene Stufe für den Inhalt von DRM-Version 1.

    | Attribut      | Wert                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | **Verwenden von \_ DRM**   | **TRUE**                                                                                    |
    | **DRM- \_ Flags** | WMT \_ right \_ Playback \| WMT \_ right \_ Copy \_ to \_ Non \_ SDMI \_ Device \| WMT \_ right \_ Copy \_ to \_ CD |
    | **DRM- \_ Ebene** | 150                                                                                         |

    

     

Der folgende Beispielcode zeigt, wie ein DRM-fähiger Writer für DRM-Version 1 erstellt und die DRM-Eigenschaften festgelegt werden. Die Fehlerüberprüfung wurde aus Gründen der Verdeutlichung ausgelassen.


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 





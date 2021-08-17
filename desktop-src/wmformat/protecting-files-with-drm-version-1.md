---
title: Schützen von Dateien mit DRM Version 1
description: Schützen von Dateien mit DRM Version 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows Medienformat-SDK, Erstellen geschützter Dateien
- Windows Medienformat-SDK, geschützte Dateien
- Advanced Systems Format (ASF), Erstellen geschützter Dateien
- ASF (Advanced Systems Format), Erstellen geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Advanced Systems Format (ASF),WMStubDRM.lib
- ASF (Advanced Systems Format), WMStubDRM.lib
- WMStubDRM.lib, Erstellen geschützter Dateien
- WMStubDRM.lib,geschützte Dateien
- Digital Rights Management (DRM), WMStubDRM.lib
- DRM (Digital Rights Management), WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b500f3711b8c92324cbd87d4dc199a8a0bb803cba69357a23f139fb96f8281f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084537"
---
# <a name="protecting-files-with-drm-version-1"></a>Schützen von Dateien mit DRM Version 1

Wenn diese Art von Schutz angewendet wird, wird eine DRM-Lizenz der Version 1 generiert, die nur auf dem Computer gültig ist, von dem aus die Lizenzanforderung gestellt wurde. Da kein Schlüssel- oder Schlüssel-Seed festgelegt ist, gibt es keine Möglichkeit, portable Lizenzen für Inhalte zu generieren, die mit diesem Verfahren geschützt werden. Wenn Sie jedoch das Windows Media Format SDK 7.1 oder höher verwenden, können die Lizenzen im Microsoft License Migration Service wiederhergestellt werden.

Führen Sie zum Schützen von ASF-Dateien mit DRM Version 1 die folgenden Schritte aus:

1.  Verknüpfen Sie die Datei WMStubDRM.lib mit Ihrem Projekt, und entlinken Sie bei Bedarf die Datei wmvcore.lib.
2.  Rufen Sie die [**WMCreateWriter-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) auf, um den Writer zu erstellen. Das erste Argument ist reserviert und muss auf NULL **festgelegt werden.**
3.  Legen Sie ein Profil fest, das vom Writer verwendet werden soll, indem [**Sie IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) oder [**IWMWriter::SetProfileByID aufrufen.**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) Sie müssen ein Profil im Writer festlegen, bevor Sie DRM-Attribute festlegen. DRM wird nur für Profile unterstützt, die Windows Medienaudio oder Windows Media Video-Codecs verwenden.
4.  Legen Sie mithilfe der [**IWMHeaderInfo::SetAttribute-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) die folgenden DRM-Eigenschaften fest. Die **Eigenschaft \_ DrM** verwenden weist die DRM-Komponenten an, den Inhalt mithilfe von DRM Version 1 zu schützen. Die **EIGENSCHAFT \_ DRM-Flags** gibt die Rechte an, die in der lokalen Lizenz enthalten sein sollen, die für den Inhalt erstellt wird. Der **DRM \_ LEVEL-Wert** wird ebenfalls in der Lizenz gespeichert. Er gibt die Mindestebene an, die für den Zugriff auf den Inhalt erforderlich ist. 150 ist die empfohlene Ebene für Inhalte der DRM-Version 1.

    | attribute      | Wert                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | **Verwenden \_ von DRM**   | **TRUE**                                                                                    |
    | **\_DRM-Flags** | WMT \_ RIGHT \_ PLAYBACK \| WMT \_ RIGHT \_ COPY \_ TO \_ NON \_ SDMI \_ DEVICE \| WMT \_ RIGHT \_ COPY \_ TO \_ CD |
    | **\_DRM-EBENE** | 150                                                                                         |

    

     

Der folgende Beispielcode zeigt, wie Sie einen DRM-fähigen Writer für DRM Version 1 erstellen und die DRM-Eigenschaften festlegen. Die Fehlerüberprüfung wurde aus Gründen der Verdeutlichung ausgelassen.


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



 

 





---
title: Installieren und Registrieren von Protokollhandlern (Legacy-Windows-Umgebungsfeatures)
description: Die Installation von Protokollhandlern umfasst das Kopieren der DLL(s) an einen geeigneten Speicherort im Verzeichnis Programme und deren Registrierung.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f6cce4337c8b2c3faf47411f76165b11ed13ff00dfebd66ac5307d6ca6a68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716560"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a>Installieren und Registrieren von Protokollhandlern (Legacy-Windows-Umgebungsfeatures)

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search.](../search/-search-3x-wds-overview.md)

Die Installation von **Protokollhandlern** umfasst das Kopieren der DLL(s) an einen geeigneten Speicherort im Verzeichnis Programme und deren Registrierung.

Dieser Abschnitt enthält die folgenden Themen:

-   [Installationsrichtlinien](#installation-guidelines)
-   [So registrieren Sie Protokollhandler](#to-register-protocol-handlers)
-   [So registrieren Sie Shellerweiterungen](#to-register-shell-extensions)

## <a name="installation-guidelines"></a>Installationsrichtlinien

Protokollhandler sollten die Selbstregistrierung für die Installation implementieren und die folgenden Richtlinien befolgen:

-   Das Installationsprogramm muss entweder EXE- oder MSI-Installer verwenden.
-   Versionshinweise müssen bereitgestellt werden.
-   Für jedes installierte Add-In muss ein Eintrag **zum Hinzufügen/Entfernen** von Programmen erstellt werden.
-   Das Installationsprogramm muss alle Registrierungseinstellungen für den jeweiligen Dateityp oder -speicher übernehmen, den das aktuelle Add-In versteht.
-   Wenn ein vorheriges Add-In überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.
-   Wenn ein neueres Add-In das vorherige Add-In überschrieben hat, sollte es die Möglichkeit geben, die Funktionalität des vorherigen Add-Ins wiederherzustellen und es wieder zum Standard-Add-In für diesen Dateityp zu machen.

## <a name="to-register-protocol-handlers"></a>So registrieren Sie Protokollhandler

Sie müssen 14 Einträge in der Registrierung vornehmen, um die Protokollhandlerkomponente zu registrieren, wobei Folgendes gilt:

-   *Ver \_ Ind \_ ProgID* ist die versionsunabhängige ProgID der Implementierung des Protokollhandlers.
-   *Ver \_ Dep \_ ProgID* ist die versionsabhängige ProgID der Implementierung des Protokollhandlers.
-   *CLSID \_ 1* ist die CLSID der Implementierung des Protokollhandlers.

1.  Registrieren Sie die versionsunabhängige ProgID mit den folgenden Schlüsseln und Werten:

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

2.  Registrieren Sie die versionsabhängige ProgID mit den folgenden Schlüsseln und Werten:

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  Registrieren Sie die CLSID des Protokollhandlers mit den folgenden Schlüsseln und Werten:

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

4.  Registrieren Sie den Protokollhandler bei Windows Desktopsuche:

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

## <a name="to-register-shell-extensions"></a>So registrieren Sie Shellerweiterungen

Sie müssen zwei Einträge in der Registrierung vornehmen, um die Shellerweiterung des Protokollhandlers zu registrieren.

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 





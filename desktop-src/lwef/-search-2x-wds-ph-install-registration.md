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
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a>Installieren und Registrieren von Protokoll Handlern (Features der Legacy-Windows-Umgebung)

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Das Installieren von **Protokoll Handlern** umfasst das Kopieren der dll (s) an einen geeigneten Speicherort im Verzeichnis "Programme" und deren Registrierung.

Dieser Abschnitt enthält die folgenden Themen:

-   [Installationsrichtlinien](#installation-guidelines)
-   [So registrieren Sie Protokollhandler](#to-register-protocol-handlers)
-   [So registrieren Sie Shellerweiterungen](#to-register-shell-extensions)

## <a name="installation-guidelines"></a>Installationsrichtlinien

Protokollhandler sollten die Selbstregistrierung für die Installation implementieren und die folgenden Richtlinien befolgen:

-   Das Installationsprogramm muss entweder exe oder das MSI-Installationsprogramm verwenden.
-   Anmerkungen zu dieser Version müssen bereitgestellt werden.
-   Ein Eintrag zum **Hinzufügen/Entfernen von Programmen** muss für jedes installierte Add-in erstellt werden.
-   Das Installationsprogramm muss alle Registrierungs Einstellungen für einen bestimmten Dateityp oder-Speicher übernehmen, den das aktuelle Add-in versteht.
-   Wenn ein vorheriges Add-in überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.
-   Wenn das vorherige Add-in von einem neueren Add-in überschrieben wurde, sollte es möglich sein, die vorherige Add-in-Funktionalität wiederherzustellen und das Standard-Add-in für diesen Dateityp erneut zu erstellen.

## <a name="to-register-protocol-handlers"></a>So registrieren Sie Protokollhandler

Sie müssen 14 Einträge in der Registrierung vornehmen, um die Protokollhandlerkomponente zu registrieren, wobei Folgendes gilt:

-   *Ver \_ IND \_ ProgID* ist die Versions unabhängige ProgID der protokollhandlerimplementierung.
-   *Ver \_ DEP \_ ProgID* ist die Versions abhängige ProgID der protokollhandlerimplementierung.
-   *CLSID \_ 1* ist die CLSID der protokollhandlerimplementierung.

1.  Registrieren Sie die Versions unabhängige ProgID mit den folgenden Schlüsseln und Werten:

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

2.  Registrieren Sie die Versions abhängige ProgID mit den folgenden Schlüsseln und Werten:

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  Registrieren Sie die CLSID des Protokoll Handlers mit den folgenden Schlüsseln und Werten:

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

4.  Registrieren Sie den Protokollhandler bei der Windows-Desktop Suche:

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

Sie müssen zwei Einträge in der Registrierung vornehmen, um die Shellerweiterung des Protokoll Handlers zu registrieren.

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 





---
title: App-Objekt-Manager (MakeAppx.exe)
description: App Packager (MakeAppx.exe) erstellt ein App-Paket aus Dateien auf dem Datenträger oder extrahiert die Dateien aus einem App-Paket auf einen Datenträger.
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41595550f3bee7b1149959886ed649e9212224b2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101467"
---
# <a name="app-packager-makeappxexe"></a>App-Objekt-Manager (MakeAppx.exe)

> [!Note]  
> Eine UWP-Anleitung zur Verwendung dieses Tools finden Sie unter [Erstellen eines App-Pakets mit dem MakeAppx.exe Tool](/windows/msix/package/create-app-package-with-makeappx-tool).

 

App Packager (MakeAppx.exe) erstellt ein App-Paket aus Dateien auf dem Datenträger oder extrahiert die Dateien aus einem App-Paket auf einen Datenträger. Ab Windows 8.1 erstellt App Packager auch ein App-Paket Paket aus app-Paketen auf einem Datenträger oder extrahiert die APP-Pakete aus einem App-Paket auf einen Datenträger. Es ist in Microsoft Visual Studio und im Windows Software Development Kit (SDK) für Windows 8 oder Windows Software Development Kit (SDK) für Windows 8.1 enthalten. Besuchen Sie [Downloads für Entwickler]( https://msdn.microsoft.com/windows/apps/br229516.aspx) , um diese zu erhalten.

Das MakeAppx.exe Tool befindet sich in der Regel an den folgenden Orten:

-   Auf x86: C: \\ Program Files (x86) \\ Windows Kits \\ 8,0 \\ bin \\ x86 \\makeappx.exe oder C: \\ Program Files (x86) \\ Windows Kits \\ 8,1 \\ bin \\ x86 \\makeappx.exe
-   Auf x64 an zwei Orten:
    -   C: \\ Programme (x86) \\ Windows Kits \\ 8,0 \\ bin \\ x86 \\makeappx.exe oder C: \\ Program Files (x86) \\ Windows Kits \\ 8,1 \\ bin \\ x86 \\makeappx.exe
    -   C: \\ Programme (x86) \\ Windows Kits \\ 8,0 \\ bin \\ x64 \\makeappx.exe oder C: \\ Program Files (x86) \\ Windows Kits \\ 8,1 \\ bin \\ x64 \\makeappx.exe

Es gibt keine Arm-Version des Tools.

-   [So erstellen Sie ein Paket mit einer Verzeichnisstruktur](#to-create-a-package-using-a-directory-structure)
-   [So erstellen Sie ein Paket mit einer Mapping-Datei](#to-create-a-package-using-a-mapping-file)
-   [So signieren Sie das Paket mit SignTool](#to-sign-the-package-using-signtool)
-   [So extrahieren Sie Dateien aus einem Paket](#to-extract-files-from-a-package)
-   [So erstellen Sie ein Paket Bündel mithilfe einer Verzeichnisstruktur](#to-create-a-package-bundle-using-a-directory-structure)
-   [So erstellen Sie ein Paket Bündel mithilfe einer Mapping-Datei](#to-create-a-package-bundle-using-a-mapping-file)
-   [So extrahieren Sie Pakete aus einem Bündel](#to-extract-packages-from-a-bundle)
-   [So verschlüsseln Sie ein Paket mit einer Schlüsseldatei](#to-encrypt-a-package-with-a-key-file)
-   [So verschlüsseln Sie ein Paket mit einem globalen Testschlüssel](#to-encrypt-a-package-with-a-global-test-key)
-   [So entschlüsseln Sie ein Paket mit einer Schlüsseldatei](#to-decrypt-a-package-with-a-key-file)
-   [So entschlüsseln Sie ein Paket mit einem globalen Testschlüssel](#to-decrypt-a-package-with-a-global-test-key)
-   [Verwendung](#usage)

## <a name="using-app-packager"></a>Verwenden von App Packager

> [!Note]  
> Relative Pfade werden im gesamten Tool unterstützt.

 

### <a name="to-create-a-package-using-a-directory-structure"></a>So erstellen Sie ein Paket mit einer Verzeichnisstruktur

Platzieren Sie die AppxManifest.xml im Stammverzeichnis eines Verzeichnisses, das alle Nutz Last Dateien für Ihre APP enthält. Eine identische Verzeichnisstruktur wird für das App-Paket erstellt und ist verfügbar, wenn das Paket zum Zeitpunkt der Bereitstellung extrahiert wird.

1.  Platzieren Sie alle Dateien in einer einzelnen Verzeichnisstruktur, und erstellen Sie nach Wunsch Unterverzeichnisse.

2.  Erstellen Sie ein gültiges Paket Manifest, AppxManifest.xml, und platzieren Sie es im Stammverzeichnis.

3.  Führen Sie den folgenden Befehl aus:

    **Makeappx Pack/d** *input \_ directerypath* **/p** _FilePath_**. AppX**

### <a name="to-create-a-package-using-a-mapping-file"></a>So erstellen Sie ein Paket mit einer Mapping-Datei

1.  Erstellen Sie ein gültiges Paket Manifest, AppxManifest.xml.

2.  Erstellen Sie eine Mapping-Datei. Die erste Zeile enthält die Zeichen folgen **\[ Dateien \]**, und in den nachfolgenden Zeilen werden die Quell-(Datenträger) und Ziel Pfade (Paket) in Zeichen folgen in Anführungszeichen angegeben.

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  Führen Sie den folgenden Befehl aus:

    **Makeappx Pack/f** *Mapping \_ FilePath* **/p** _FilePath_**. AppX**

### <a name="to-sign-the-package-using-signtool"></a>So signieren Sie das Paket mit SignTool

1.  Erstellen Sie das Zertifikat. Der im Manifest aufgelistete Verleger muss mit den Informationen des Verleger Antragstellers des Signatur Zertifikats identisch sein. Weitere Informationen zum Erstellen eines Signatur Zertifikats finden Sie unter [Erstellen eines App-Paket-Signatur Zertifikats](how-to-create-a-package-signing-certificate.md).

2.  Führen Sie SignTool.exe aus, um das Paket zu signieren:

    **SignTool Sign/a/v/FD** *HashAlgorithm* **/f** *certfilename* _FilePath_**. AppX**

    *HashAlgorithm* muss mit dem Hash Algorithmus, der zum Erstellen der blockmap verwendet wurde, beim Verpacken der App entsprechen. Mit dem Hilfsprogramm makeappx-Paket ist der standardmäßige AppX blockmap-Hash Algorithmus **SHA256**. Führen Sie SignTool.exe mit Angabe von **SHA256** als File Digest-Algorithmus (/FD) aus:

    **SignTool Sign/a/v/FD SHA256/f** *certfilename* _FilePath_**. AppX**

    Weitere Informationen zum Signieren von Paketen finden Sie unter [Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md).

### <a name="to-extract-files-from-a-package"></a>So extrahieren Sie Dateien aus einem Paket

1.  Führen Sie den folgenden Befehl aus:

    **Makeappx entpacken/p** _File_**. AppX/d** *Ausgabe \_ Verzeichnis*

2.  Das entpackte Paket hat die gleiche Struktur wie das installierte Paket.

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a>So erstellen Sie ein Paket Bündel mithilfe einer Verzeichnisstruktur

Wir verwenden den **Bundle** -Befehl, um eine APP Bundle zu erstellen. <output bundle name> durch das Hinzufügen aller Pakete aus <content directory> (einschließlich Unterordnern). Wenn <content directory> ein Bündel Manifest enthält, wird AppxBundleManifest.xml ignoriert.

1.  Platzieren Sie alle Pakete in einer einzelnen Verzeichnisstruktur, und erstellen Sie nach Wunsch Unterverzeichnisse.

2.  Führen Sie den folgenden Befehl aus:

    **Makeappx Bundle/d** *input \_ directoriypath* **/p** _FilePath_**. appxbundle**

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a>So erstellen Sie ein Paket Bündel mithilfe einer Mapping-Datei

Wir verwenden den **Bundle** -Befehl, um eine APP Bundle zu erstellen. <output bundle name> durch das Hinzufügen aller Pakete aus einer Liste von Paketen in <mapping file> . Wenn <mapping file> ein Bündel Manifest enthält, wird AppxBundleManifest.xml ignoriert.

1.  Erstellen Sie eine <mapping file>. Die erste Zeile enthält die Zeichen folgen **\[ Dateien \]**, und in den folgenden Zeilen werden die Pakete angegeben, die dem Paket hinzugefügt werden sollen. Jedes Paket wird durch ein paar von Pfaden in Anführungszeichen, getrennt durch Leerzeichen oder Registerkarten, beschrieben. Das Pfad paar stellt die Quelle des Pakets (auf dem Datenträger) und das Ziel (in Bundle) dar. Alle Ziel Paketnamen müssen die Erweiterung ". AppX" aufweisen.

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  Führen Sie den folgenden Befehl aus:

    **Makeappx Bundle/f** *Mapping \_ FilePath* **/p** _FilePath_**. appxbundle**

### <a name="to-extract-packages-from-a-bundle"></a>So extrahieren Sie Pakete aus einem Bündel

1.  Führen Sie den folgenden Befehl aus:

    **Makeappx entflechten/p** _Bundle \_ Name_**. appxbundle/d** *Ausgabe \_ Verzeichnis*

2.  Das entpackte Paket hat die gleiche Struktur wie das installierte Paket Paket.

### <a name="to-encrypt-a-package-with-a-key-file"></a>So verschlüsseln Sie ein Paket mit einer Schlüsseldatei

1.  Erstellen Sie eine Schlüsseldatei. Schlüsseldateien müssen mit einer Zeile beginnen, die die Zeichenfolge " \[ Keys \] " enthält, gefolgt von Zeilen, in denen die Schlüssel zum Verschlüsseln des Pakets beschrieben werden. Jeder Schlüssel wird durch ein paar von Zeichen folgen in Anführungszeichen, getrennt durch Leerzeichen oder Tabstopps, beschrieben. Die erste Zeichenfolge stellt die Schlüssel-ID dar, und die zweite Zeichenfolge stellt den Verschlüsselungsschlüssel in hexadezimaler Form dar.

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  Führen Sie den folgenden Befehl aus:

    **MakeAppx.exe verschlüsseln/p** _\_ Paketname_**. AppX/EP** _verschlüsselter \_ \_ Paketname_.**eappx/KF** _KeyFile \_ Name_**. txt**

3.  Das Eingabe Paket wird mithilfe der angegebenen Schlüsseldatei in das angegebene verschlüsselte Paket verschlüsselt.

### <a name="to-encrypt-a-package-with-a-global-test-key"></a>So verschlüsseln Sie ein Paket mit einem globalen Testschlüssel

1.  Führen Sie den folgenden Befehl aus:

    **MakeAppx.exe verschlüsseln/p** _\_ Paketname_**. AppX/EP** _verschlüsselter \_ \_ Paketname_**. eappx/KT**

2.  Das Eingabe Paket wird mithilfe des globalen Test Schlüssels in das angegebene verschlüsselte Paket verschlüsselt.

### <a name="to-decrypt-a-package-with-a-key-file"></a>So entschlüsseln Sie ein Paket mit einer Schlüsseldatei

1.  Erstellen Sie eine Schlüsseldatei. Schlüsseldateien müssen mit einer Zeile beginnen, die die Zeichenfolge " \[ Keys \] " enthält, gefolgt von Zeilen, in denen die Schlüssel zum Verschlüsseln des Pakets beschrieben werden. Jeder Schlüssel wird durch ein paar von Zeichen folgen in Anführungszeichen, getrennt durch Leerzeichen oder Tabstopps, beschrieben. Die erste Zeichenfolge stellt die Base64-codierte 32-Byte-Schlüssel-ID und die zweite Zeichenfolge den Base64-codierten 32-Byte-Verschlüsselungsschlüssel dar.

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  Führen Sie den folgenden Befehl aus:

    **MakeAppx.exe entschlüsseln/p** _\_ Paketname_**. AppX/EP** _unverschlüsselter \_ \_ Paketname_**. eappx/KF** _KeyFile \_ Name_**. txt**

3.  Das Eingabe Paket wird mithilfe der angegebenen Schlüsseldatei in das angegebene unverschlüsselte Paket entschlüsselt.

### <a name="to-decrypt-a-package-with-a-global-test-key"></a>So entschlüsseln Sie ein Paket mit einem globalen Testschlüssel

1.  Führen Sie den folgenden Befehl aus:

    **MakeAppx.exe entschlüsseln/p** _\_ Paketname_**. AppX/EP** _unverschlüsselter \_ \_ Paketname_**. eappx/KT**

2.  Das Eingabe Paket wird mithilfe des globalen Test Schlüssels in das angegebene unverschlüsselte Paket entschlüsselt.

## <a name="usage"></a>Verbrauch

Das Befehlszeilenargument **/p** ist immer erforderlich, entweder mit **/d**, **/f** oder **/EP**. Beachten Sie, dass sich **/d**, **/f** und **/EP** gegenseitig ausschließen.

**Makeappx Pack \[ - \] Optionen** **/p** *\<output package name\>* **/d***\<content directory\>*

**Makeappx Pack \[ - \] Optionen** **/p** *\<output package name\>* **/f***\<mapping file\>*

**Makeappx entpacken \[ - \] Optionen** **/p** *\<input package name\>* **/d***\<output directory\>*

**Makeappx- \[ Bündel \] Optionen** **/p** *\<output bundle name\>* **/d***\<content directory\>*

**Makeappx- \[ Bündel \] Optionen** **/p** *\<output bundle name\>* **/f***\<mapping file\>*

**Makeappx entflechten \[ - \] Optionen** **/p** *\<input bundle name\>* **/d***\<output directory\>*

**Makeappx- \[ Verschlüsselungs \] Optionen** **/p** *\<input package name\>* **/EP***\<output package name\>*

**Makeappx- \[ \] Entschlüsselungen** **/p** *\<input package name\>* **/EP***\<output package name\>*

## <a name="command-line-syntax"></a>Befehlszeilensyntax

Hier ist die allgemeine Syntax Syntax für die Befehlszeile für makeappx.

**Makeappx \[ Pack \| Entpacken \| des Pakets \| \| \| \] entflechten verschlüsseln** \[ **/h** **/KF** **/KT** **/l** **/o** **/No** **/NV** **/v** **/PFN** **/?**\]

**Makeappx** verpackt bzw. entpackt die Dateien in einem Paket, bündelt oder entpackt die Pakete in einem Paket oder verschlüsselt oder entschlüsselt das App-Paket oder Paket im angegebenen Eingabe Verzeichnis bzw. in der Zuordnungsdatei. Im folgenden finden Sie eine Liste der Parameter, die für **makeappx Pack**, **makeappx entpacken**, **makeappx Bundle**, **makeappx entflechten**, **makeappx verschlüsseln** oder **makeappx entschlüsseln** gelten.

<dl> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

Diese Option wird für lokalisierte Pakete verwendet. Die Standardüberprüfung wird durch lokalisierte Pakete ausgelöst. Mit dieser Option wird nur diese spezifische Validierung deaktiviert, ohne dass die gesamte Validierung deaktiviert werden muss.

</dd> <dt>

<span id="_o"></span><span id="_O"></span>**/o**
</dt> <dd>

Überschreiben Sie die Ausgabedatei, falls vorhanden. Wenn Sie diese Option oder die Option **/No** nicht angeben, wird der Benutzer gefragt, ob die Datei überschrieben werden soll.

Sie können diese Option nicht mit **/No** verwenden.

</dd> <dt>

<span id="_no"></span><span id="_NO"></span>**/no**
</dt> <dd>

Verhindert ein Überschreiben der Ausgabedatei, wenn vorhanden. Wenn Sie diese Option oder die Option **/o** nicht angeben, wird der Benutzer gefragt, ob die Datei überschrieben werden soll.

Sie können diese Option nicht mit **/o** verwenden.

</dd> <dt>

<span id="_nv"></span><span id="_NV"></span>**/nv**
</dt> <dd>

Überspringen der semantischen Validierung. Wenn Sie diese Option nicht angeben, führt das Tool eine vollständige Überprüfung des Pakets aus.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Aktivieren Sie die ausführliche Protokollierungs Ausgabe in der Konsole.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Hilfetext anzeigen.

</dd> </dl>

**Makeappx Pack** , **makeappx entpacken** , **makeappx Bundle**, **makeappx entflechten**, **makeappx verschlüsseln** und **makeappx entschlüsseln** sind sich gegenseitig ausschließende Befehle. Hier sind die Befehlszeilenparameter aufgeführt, die speziell für jeden Befehl gelten:

**Makeappx-Paket** \[ **h**\]

Erstellt ein Paket.

<dl> <dt>

<span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** - *Algorithmus*
</dt> <dd>

Gibt den Hashalgorithmus an, der beim Erstellen der Blockzuordnung verwendet wird. Im folgenden finden Sie gültige Werte für den- *Algorithmus*:

<dl> <dd>SHA256 (Standard)</dd> <dd>SHA384</dd> <dd>SHA512</dd> </dl>

Diese Option kann nicht mit dem **Entpacken** -Befehl verwendet werden.

</dd> </dl>

**Makeappx entpacken** \[ **PFN**\]

Extrahiert alle Dateien im angegebenen Paket in das angegebene Ausgabeverzeichnis. Die Ausgabe hat dieselbe Verzeichnisstruktur wie das Paket.

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

Gibt ein Verzeichnis namens mit dem vollständigen Paketnamen an. Dieses Verzeichnis wird unter dem angegebenen Ausgabe Speicherort erstellt. Diese Option kann nicht mit dem Befehl **Pack** verwendet werden.

</dd> </dl>

**Makeappx-Paket** \[ Entpacken **PFN**\]

Entpackt alle Pakete in ein Unterverzeichnis unter dem angegebenen Ausgabepfad, benannt nach dem vollständigen Paketnamen. Die Ausgabe hat dieselbe Verzeichnisstruktur wie das Paket mit installiertem Paket.

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

Gibt ein Verzeichnis mit dem Namen des Paket Bündel vollständig an. Dieses Verzeichnis wird unter dem angegebenen Ausgabe Speicherort erstellt. Diese Option kann nicht mit dem **Bundle** -Befehl verwendet werden.

</dd> </dl>

**Makeappx verschlüsseln** \[ **KF**, **KT**\]

Erstellt im angegebenen Ausgabe Paket ein verschlüsseltes App-Paket aus dem angegebenen Eingabe-App-Paket.

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/KF***<key file>*
</dt> <dd>

Verschlüsselt das Paket oder Paket mithilfe des Schlüssels aus der angegebenen Schlüsseldatei. Diese Option kann nicht mit **KT** verwendet werden.

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

Verschlüsselt das Paket oder Paket mit dem globalen Testschlüssel. Diese Option kann nicht mit **KF** verwendet werden.

</dd> </dl>

**Makeappx-Entschlüsselung** \[ **KF**, **KT**\]

Erstellt ein unverschlüsseltes App-Paket aus dem angegebenen Eingabe-App-Paket im angegebenen Ausgabe Paket.

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/KF***<key file>*
</dt> <dd>

Entschlüsselt das Paket oder Paket mithilfe des Schlüssels aus der angegebenen Schlüsseldatei. Diese Option kann nicht mit **KT** verwendet werden.

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

Entschlüsselt das Paket oder Paket mit dem globalen Testschlüssel. Diese Option kann nicht mit **KF** verwendet werden.

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a>Durch makeappx ausgeführte Semantik Validierung

Makeappx führt eine eingeschränkte Semantik Überprüfung durch, mit der die häufigsten Bereitstellungs Fehler abgefangen und sichergestellt werden, dass das App-Paket gültig ist.

Diese Überprüfung stellt Folgendes sicher:

-   Alle Dateien, auf die im Paketmanifest verwiesen wird, sind im App-Paket enthalten.
-   Die Anwendung besitzt nicht zwei identische Schlüssel.
-   Eine Anwendung registriert sich nicht für ein unzulässiges Protokoll aus dieser Liste: SMB, File, MS-WWA-Web, MS-WWA.

Diese semantische Validierung ist nicht fertiggestellt, und die von makeappx erstellten Pakete sind nicht garantiert installier Bar.

 

 
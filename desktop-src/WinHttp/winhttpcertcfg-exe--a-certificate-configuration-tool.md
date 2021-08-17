---
description: Mit dem Zertifikatkonfigurationstool microsoft Windows HTTP Services (WinHTTP) &\# 0034;WinHttpCertCfg.exe&0034; können Administratoren Clientzertifikate in jedem Zertifikatspeicher installieren und konfigurieren, auf den das \# Internet Server Web Application Manager-Konto (IWAM) zugreifen kann. Das Tool entfällt auch die Notwendigkeit, besondere Maßnahmen für Konten wie das IWAM-Konto zu unternehmen, um zugriff auf Zertifikate zu erhalten, wenn sie Active Server Pages (ASP) verwenden.
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, ein Zertifikatkonfigurationstool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ce9978f6e2ffcafa1357a45dbeff80c12bf0e6ea2f7f3fb9656376b33dfb23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743798"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a>WinHttpCertCfg.exe, ein Zertifikatkonfigurationstool

Mit dem [Zertifikatkonfigurationstool "WinHttpCertCfg.exe" von Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) können Administratoren Clientzertifikate [](glossary.md) in jedem Zertifikatspeicher installieren und konfigurieren, auf den das Internet Server Web Application Manager-Konto (IWAM) zugreifen kann. Das Tool entfällt auch die Notwendigkeit, besondere Maßnahmen für Konten wie das IWAM-Konto zu unternehmen, um zugriff auf Zertifikate zu erhalten, wenn sie Active Server Pages (ASP) verwenden.

Mit Microsoft Management Console (MMC) können Administratoren Clientzertifikate auf einen lokalen Computer importieren. Beim Importieren eines Zertifikats wird jedoch nicht automatisch Zugriff auf den privaten Schlüssel für andere Konten gewährt. Dieser private Schlüssel ist für die Clientzertifikatauthentifizierung erforderlich. Das WinHTTP-Zertifikatkonfigurationstool (Microsoft Windows HTTP Services) bietet die Möglichkeit, bei Bedarf Zugriff auf zusätzliche Konten wie das IWAM-Konto zu gewähren.

-   [Verwenden des Zertifikatkonfigurationstools](#using-the-certificate-configuration-tool)
-   [Beispiele](#examples)

## <a name="using-the-certificate-configuration-tool"></a>Verwenden des Zertifikatkonfigurationstools

Das WinHTTP-Zertifikatkonfigurationstool WinHttpCertCfg.exe steht als Download auf der Windows [Server 2003 Resource Kit Tools-Website zur](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) Verfügung. Der folgende Beispielcode zeigt die gültigen Befehlszeilenparameter, die mit diesem Tool verwendet werden können.

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

In der folgenden Tabelle sind die Parameter für das Konfigurationstool aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>Zeigt Syntaxdaten an.</td>
</tr>
<tr class="even">
<td>-i</td>
<td>Gibt an, dass das Zertifikat aus einer PFX-Datei (Personal Information Exchange) importiert werden soll. Auf diesen Parameter muss der Name der Datei folgen. Wenn dieser Parameter angegeben wird, &quot; müssen -a &quot; und &quot; -c ebenfalls angegeben &quot; werden.</td>
</tr>
<tr class="odd">
<td>-g</td>
<td>Gibt an, dass zugriff auf einen privaten Schlüssel gewährt wird. Wenn dieser Parameter angegeben wird, &quot; müssen &quot; -a, &quot; -c und &quot; &quot; -s ebenfalls angegeben &quot; werden.</td>
</tr>
<tr class="even">
<td>-r</td>
<td>Gibt an, dass der Zugriff für einen privaten Schlüssel entfernt wird. Wenn dieser Parameter angegeben wird, &quot; müssen &quot; -a, &quot; -c und &quot; &quot; -s ebenfalls angegeben &quot; werden.</td>
</tr>
<tr class="odd">
<td>-l</td>
<td>Gibt an, dass Konten mit Zugriff auf einen privaten Schlüssel aufgelistet werden. Wenn dieser Parameter angegeben wird, &quot; müssen -c &quot; und &quot; -s ebenfalls angegeben &quot; werden.</td>
</tr>
<tr class="even">
<td>-a</td>
<td>Gibt das Benutzerkonto auf dem Computer an, der konfiguriert wird. Dies kann ein lokaler Computer oder ein Domänenkonto sein, z. B. &quot; IWAM_TESTMACHINE &quot; , &quot; TESTUSER &quot; oder &quot; TESTDOMAIN\DOMAINUSER &quot; .</td>
</tr>
<tr class="odd">
<td>-c</td>
<td>Gibt den Speicherort und den Namen des <a href="glossary.md"><em>Zertifikatspeichers an.</em></a> Verwenden &quot; LOCAL_MACHINE &quot; oder &quot; &quot; CURRENT_USER, um zu bestimmen, welcher Registrierungszweig für den Speicherort verwendet werden soll. Der <em>Zertifikatspeicher</em> kann ein beliebiger auf dem Computer installierter sein. Typische Namensbeispiele sind &quot; &quot; MY, &quot; Root und &quot; &quot; &quot; TrustedPeople. Speicherort und Name <em></em> des Zertifikatspeichers sind durch einen rückwärts gerichteten Schrägstrich getrennt, z. B. &quot; LOCAL_MACHINE\Root. &quot;
<blockquote>
[!Note]<br />
Obwohl der CURRENT_USER-Branch der Registrierung mit diesem Parameter angegeben werden kann, ist die Erweiterung des Zugriffs auf private Schlüssel in erster Linie für Zertifikate vorgesehen, die in einem Zertifikatspeicher eines lokalen Computers installiert sind, auf den mehrere Benutzer zugreifen &quot; &quot; können. <a href="glossary.md"><em></em></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>-S</td>
<td>Gibt eine Suchzeichenfolge an, bei der die Groß-/Kleinschreibung nicht beachtet wird, um das erste aufzählte Zertifikat mit einem Betreffnamen zu suchen, der diese Teilzeichenfolge enthält.</td>
</tr>
<tr class="odd">
<td>-p</td>
<td>Gibt ein Kennwort an, das zum Importieren des Zertifikats und des privaten Schlüssels verwendet wird. Dies wird nur mit der Importoption verwendet.</td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> Der Benutzer muss über ausreichende Berechtigungen verfügen, um dieses Tool verwenden zu können. Daher muss der Benutzer Administrator und derselbe Benutzer sein, der das Clientzertifikat installiert hat( sofern installiert).
>
> Das "WinHttpCertCfg.exe"-Tool ist nicht nützlich, um Zertifikate zu konfigurieren, die in einem Dateisystem wie FAT32 gespeichert sind, das keine Zugriffssteuerungslisten (Access Control Lists, ACL) unterstützt.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen einige der Möglichkeiten, wie das Konfigurationstool verwendet werden kann.

1.  Dieser Befehl listet Konten auf, die Zugriff auf den privaten Schlüssel für [](glossary.md) das Zertifikat "MyCertificate" im Zertifikatspeicher "Root" des Branchs LOCAL MACHINE der \_ Registrierung haben.

    **winhttpcertcfg -l -c LOCAL \_ MACHINE \\ Root -s MyCertificate**

2.  Dieser Befehl gewährt Zugriff auf den privaten Schlüssel des Zertifikats "MyCertificate" im Zertifikatspeicher [*"My"*](glossary.md) für das TESTUSER-Konto.

    **winhttpcertcfg -g -c LOCAL \_ MACHINE \\ My -s MyCertificate -a TESTUSER**

3.  Dieser Befehl importiert ein Zertifikat und einen privaten Schlüssel aus einer PFX-Datei und erweitert den Zugriff auf einen privaten Schlüssel auf ein anderes Konto.

    **winhttpcertcfg -i PFXFile -c LOCAL \_ MACHINE \\ My -a IWAM \_ TESTMACHINE -p PFXPassword**

4.  Dieser Befehl verweigert den Zugriff auf den privaten Schlüssel für das IWAM \_ TESTMACHINE-Konto mit dem angegebenen Zertifikat.

    **winhttpcertcfg -r -c LOCAL \_ MACHINE \\ Root -s MyCertificate -a IWAM \_ TESTMACHINE**

 

 





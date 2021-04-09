---
description: Das Microsoft Windows HTTP-Dienste (WinHTTP) Certificate Configuration Tool &\# 0034; WinHttpCertCfg.exe&\# 0034; ermöglicht Administratoren das Installieren und Konfigurieren von Client Zertifikaten in einem beliebigen Zertifikat Speicher, auf den über das Internet Server Web Application Manager-Konto (IWAM) zugegriffen werden kann. Außerdem entfällt das Tool darauf, dass Sie spezielle Konten, wie z. b. das IWAM-Konto, benötigen, um bei Verwendung von Active Server Pages (ASP) Zugriff auf Zertifikate zu erhalten.
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, ein Zertifikat Konfigurations Tool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4250cd717b9f611f4f23f17c93069760c283c97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129252"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a>WinHttpCertCfg.exe, ein Zertifikat Konfigurations Tool

Das [Microsoft Windows HTTP-Dienste (WinHTTP)](about-winhttp.md) -Zertifikat Konfigurationstool "WinHttpCertCfg.exe" ermöglicht es Administratoren, Client Zertifikate in einem beliebigen [*Zertifikat Speicher*](glossary.md) zu installieren und zu konfigurieren, auf den über das Internet Server Web Application Manager-Konto (IWAM) zugegriffen werden kann. Außerdem entfällt das Tool darauf, dass Sie spezielle Konten, wie z. b. das IWAM-Konto, benötigen, um bei Verwendung von Active Server Pages (ASP) Zugriff auf Zertifikate zu erhalten.

Mithilfe der Microsoft Management Console (MMC) können Administratoren Client Zertifikate auf einen lokalen Computer importieren. Beim Importieren eines Zertifikats wird jedoch nicht automatisch der Zugriff auf den privaten Schlüssel für andere Konten gewährt. Dieser private Schlüssel ist für die Client Zertifikat Authentifizierung erforderlich. Das Microsoft Windows HTTP-Dienste (WinHTTP)-Zertifikat Konfigurationstool bietet die Möglichkeit, den Zugriff auf zusätzliche Konten (z. b. das IWAM-Konto) zu gewähren, wenn dies erforderlich ist.

-   [Verwenden des Zertifikat Konfigurationstools](#using-the-certificate-configuration-tool)
-   [Beispiele](#examples)

## <a name="using-the-certificate-configuration-tool"></a>Verwenden des Zertifikat Konfigurationstools

Das WinHTTP-Zertifikat Konfigurationstool (WinHttpCertCfg.exe) steht als Download auf der [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) -Website zur Verfügung. Der folgende Beispielcode zeigt die gültigen Befehlszeilenparameter, die mit diesem Tool verwendet werden sollen.

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

In der folgenden Tabelle sind die Parameter für das-Konfigurationstool aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>Zeigt Syntax Daten an.</td>
</tr>
<tr class="even">
<td>-i</td>
<td>Gibt an, dass das Zertifikat aus einer PFX-Datei (Personal Information Exchange) importiert werden soll. Auf diesen Parameter muss der Name der Datei folgen. Wenn dieser Parameter angegeben wird, &quot; &quot; müssen auch-a und &quot; -c &quot; angegeben werden.</td>
</tr>
<tr class="odd">
<td>-g</td>
<td>Gibt an, dass der Zugriff auf einen privaten Schlüssel gewährt wird. Wenn dieser Parameter angegeben ist, &quot; müssen-a &quot; , &quot; -c &quot; und &quot; -s &quot; ebenfalls angegeben werden.</td>
</tr>
<tr class="even">
<td>-r</td>
<td>Gibt an, dass der Zugriff für einen privaten Schlüssel entfernt wird. Wenn dieser Parameter angegeben ist, &quot; müssen-a &quot; , &quot; -c &quot; und &quot; -s &quot; ebenfalls angegeben werden.</td>
</tr>
<tr class="odd">
<td>-l</td>
<td>Gibt an, dass Konten mit Zugriff auf einen privaten Schlüssel aufgelistet werden. Wenn dieser Parameter angegeben wird, &quot; &quot; müssen auch-c und &quot; -s &quot; angegeben werden.</td>
</tr>
<tr class="even">
<td>-a</td>
<td>Gibt das Benutzerkonto auf dem Computer an, der konfiguriert wird. Dabei kann es sich um ein lokales Computer-oder Domänen Konto handeln, wie z &quot; &quot; . b. IWAM_TESTMACHINE, &quot; testuser &quot; oder &quot; testdomain\domainuser &quot; .</td>
</tr>
<tr class="odd">
<td>-c</td>
<td>Gibt den Speicherort und den Namen des <a href="glossary.md"><em>Zertifikat Speicher</em></a>an. Verwenden &quot; &quot; Sie LOCAL_MACHINE oder &quot; CURRENT_USER &quot; , um zu bestimmen, welcher registrierungsbranch für den Speicherort verwendet werden soll. Der <em>Zertifikat Speicher</em> kann alle auf dem Computer installiert sein. Typische namens Beispiele sind &quot; My &quot; , &quot; root &quot; und &quot; treuhändpeople &quot; . Der Speicherort und der Name des <em>Zertifikat Speicher</em> sind durch einen umgekehrten Schrägstrich getrennt, z &quot; . b. LOCAL_MACHINE \Root &quot; .
<blockquote>
[!Note]<br />
Obwohl der &quot; CURRENT_USER &quot; Branch der Registrierung mit diesem Parameter angegeben werden kann, ist das Erweitern des Zugriffs auf private Schlüssel hauptsächlich für Zertifikate vorgesehen, die in einem <a href="glossary.md"><em>Zertifikat Speicher</em></a> des lokalen Computers installiert sind und auf den von mehreren Benutzern zugegriffen werden kann.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>-S</td>
<td>Gibt eine Such Zeichenfolge ohne Beachtung der Groß-/Kleinschreibung für die Suche nach dem ersten aufgelisteten Zertifikat mit einem Antragsteller Namen an</td>
</tr>
<tr class="odd">
<td>-p</td>
<td>Gibt ein Kennwort an, das verwendet wird, um das Zertifikat und den privaten Schlüssel zu importieren. Diese Option wird nur mit der Import-Option verwendet.</td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> Der Benutzer muss über ausreichende Berechtigungen verfügen, um dieses Tool verwenden zu können. Dies erfordert, dass der Benutzer ein Administrator und derselbe Benutzer ist, der das Client Zertifikat installiert hat, sofern es installiert ist.
>
> Das Tool "WinHttpCertCfg.exe" ist nicht nützlich, um in einem Dateisystem wie FAT32 gespeicherte Zertifikate zu konfigurieren, die keine Zugriffs Steuerungs Listen (Access Control Lists, ACL) unterstützen.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen einige Möglichkeiten, wie das-Konfigurationstool verwendet werden kann.

1.  Mit diesem Befehl werden Konten aufgelistet, die Zugriff auf den privaten Schlüssel für das Zertifikat "myCertificate" im [*Zertifikat Speicher*](glossary.md) "root" des lokalen \_ Computer Branchs der Registrierung haben.

    **Winhttpcertcfg-l-c lokale \_ Computer Stamm \\ -s myCertificate**

2.  Mit diesem Befehl wird der Zugriff auf den privaten Schlüssel des Zertifikats "myCertificate" im [*Zertifikat Speicher*](glossary.md) "My" für das testuser-Konto gewährt.

    **Winhttpcertcfg-g-c lokaler \_ Computer \\ My-s myCertificate-a testuser**

3.  Dieser Befehl importiert ein Zertifikat und einen privaten Schlüssel aus einer PFX-Datei und erweitert den privaten Schlüssel Zugriff auf ein anderes Konto.

    **Winhttpcertcfg-i pfxfile-c lokaler \_ Computer \\ My-a IWAM \_ testmachine-p pfxpassword**

4.  Dieser Befehl verweigert den Zugriff auf den privaten Schlüssel für das IWAM- \_ testmachine-Konto mit dem angegebenen Zertifikat.

    **Winhttpcertcfg-r-c lokale \_ Computer Stamm \\ -s myCertificate-a IWAM \_ testmachine**

 

 





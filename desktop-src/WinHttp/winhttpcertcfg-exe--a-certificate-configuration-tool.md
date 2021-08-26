---
description: Mit dem Zertifikatkonfigurationstool microsoft Windows HTTP Services (WinHTTP) &\# 0034;WinHttpCertCfg.exe&0034; können Administratoren Clientzertifikate in jedem Zertifikatspeicher installieren und konfigurieren, auf den das \# Internet Server Web Application Manager-Konto (IWAM) zugreifen kann. Das Tool entfällt auch die Notwendigkeit, besondere Maßnahmen für Konten wie das IWAM-Konto zu unternehmen, um zugriff auf Zertifikate zu erhalten, wenn Sie Active Server Pages (ASP) verwenden.
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, ein Zertifikatkonfigurationstool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b8fbfadd6cf0282f63b26c8dd40d5ef96b5f54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466427"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a>WinHttpCertCfg.exe, ein Zertifikatkonfigurationstool

Mit dem [Zertifikatkonfigurationstool "WinHttpCertCfg.exe" von Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) können Administratoren Clientzertifikate [](glossary.md) in jedem Zertifikatspeicher installieren und konfigurieren, auf den das Internet Server Web Application Manager-Konto (IWAM) zugreifen kann. Das Tool entfällt auch die Notwendigkeit, besondere Maßnahmen für Konten wie das IWAM-Konto zu unternehmen, um zugriff auf Zertifikate zu erhalten, wenn Sie Active Server Pages (ASP) verwenden.

Mit Microsoft Management Console (MMC) können Administratoren Clientzertifikate auf einen lokalen Computer importieren. Beim Importieren eines Zertifikats wird jedoch nicht automatisch Zugriff auf den privaten Schlüssel für andere Konten gewährt. Dieser private Schlüssel ist für die Clientzertifikatauthentifizierung erforderlich. Das Microsoft Windows-Zertifikatkonfigurationstool (WinHTTP) bietet die Möglichkeit, bei Bedarf Zugriff auf zusätzliche Konten zu gewähren, z. B. das IWAM-Konto.

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




| Parameter | BESCHREIBUNG | 
|-----------|-------------|
| -? | Zeigt Syntaxdaten an. | 
| -i | Gibt an, dass das Zertifikat aus einer PFX-Datei (Personal Information Exchange) importiert werden soll. Auf diesen Parameter muss der Name der Datei folgen. Wenn dieser Parameter angegeben wird, müssen auch "-a" und "-c" angegeben werden. | 
| -g | Gibt an, dass zugriff auf einen privaten Schlüssel gewährt wird. Wenn dieser Parameter angegeben wird, müssen auch "-a", "-c" und "-s" angegeben werden. | 
| -r | Gibt an, dass der Zugriff für einen privaten Schlüssel entfernt wird. Wenn dieser Parameter angegeben wird, müssen auch "-a", "-c" und "-s" angegeben werden. | 
| -l | Gibt an, dass Konten mit Zugriff auf einen privaten Schlüssel aufgelistet werden. Wenn dieser Parameter angegeben wird, müssen auch "-c" und "-s" angegeben werden. | 
| -a | Gibt das Benutzerkonto auf dem Computer an, der konfiguriert wird. Dies kann ein lokaler Computer oder ein Domänenkonto sein, z. B. "IWAM_TESTMACHINE", "TESTUSER" oder "TESTDOMAIN\DOMAINUSER". | 
| -c | Gibt den Speicherort und den Namen des <a href="glossary.md"><em>Zertifikatspeichers an.</em></a> Verwenden Sie "LOCAL_MACHINE" oder "CURRENT_USER", um zu bestimmen, welcher Registrierungszweig für den Speicherort verwendet werden soll. Der <em>Zertifikatspeicher</em> kann ein beliebiger auf dem Computer installierter sein. Typische Namensbeispiele sind "MY", "Root" und "TrustedPeople". Speicherort und Name des <em>Zertifikatspeichers</em> sind durch einen rückwärts gerichteten Schrägstrich getrennt, z. B. "LOCAL_MACHINE\Root".<blockquote>[!Note]<br />Obwohl der "CURRENT_USER"-Branch der Registrierung mit diesem Parameter angegeben werden kann, ist die Erweiterung des Zugriffs <a href="glossary.md"><em></em></a> auf private Schlüssel in erster Linie für Zertifikate vorgesehen, die in einem Zertifikatspeicher eines lokalen Computers installiert sind, auf die mehrere Benutzer zugreifen können.</blockquote><br /> | 
| -S | Gibt eine Suchzeichenfolge an, bei der die Groß-/Kleinschreibung nicht beachtet wird, um das erste aufzählte Zertifikat mit einem Betreffnamen zu suchen, der diese Teilzeichenfolge enthält. | 
| -p | Gibt ein Kennwort an, das zum Importieren des Zertifikats und des privaten Schlüssels verwendet wird. Dies wird nur mit der Importoption verwendet. | 




 

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

 

 





---
description: Erläutert die Verwendung von SignTool zum Signieren einer Datei.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: SignTool zum Signieren einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d8e85e8e22f65ccbe8b5f15453b0a0cac34fc27697bad648b1c815f255b10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971470"
---
# <a name="using-signtool-to-sign-a-file"></a>SignTool zum Signieren einer Datei

Der folgende Befehl signiert die Datei MyControl.exe [](../secgloss/c-gly.md) mithilfe eines Zertifikats, das in einer PFX-Datei (Personal Information Exchange) gespeichert ist:

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

Der folgende Befehl signiert die Datei mithilfe eines Zertifikats, das in einer kennwortgeschützten PFX-Datei gespeichert ist:

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> Stellen Sie sicher, dass Sie das Kennwort ordnungsgemäß schützen.

 

Mit dem folgenden Befehl wird die Datei signiert und mit einem Zeitstempel versehen:

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> Informationen zum Zeitstempeln einer Datei, nachdem sie bereits signiert wurde, finden Sie unter Hinzufügen von [Zeitstempeln zu zuvor signierten Dateien.](adding-time-stamps-to-previously-signed-files.md)

 

Der folgende Befehl signiert die Datei mithilfe eines Zertifikats, das sich im Speicher My befindet, mit dem Betreffnamen My Company Publisher:

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

Der folgende Befehl signiert ein ActiveX-Steuerelement und stellt Informationen zur Verfügung, die von Internet Explorer angezeigt werden, wenn der Benutzer aufgefordert wird, das Steuerelement zu installieren:

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

Der folgende Befehl signiert die Datei mithilfe eines Zertifikats, dessen [*Private Key-Informationen*](../secgloss/p-gly.md) durch ein Hardwarekryptografiemodul geschützt sind. Angenommen, das Zertifikat mit dem Namen "Mein High-Value-Zertifikat" verfügt über einen privaten Schlüssel, der in einem Hardwarekryptografiemodul installiert ist, und das Zertifikat ist ordnungsgemäß installiert.

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

Der folgende Befehl signiert die Datei mithilfe eines Zertifikats, dessen [*Private Key-Informationen*](../secgloss/p-gly.md) durch ein Hardwarekryptografiemodul geschützt sind. Ein Computerspeicher wird für den [*Zertifizierungsstellenspeicher*](../secgloss/c-gly.md) angegeben.

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

Der folgende Befehl signiert die Datei mithilfe eines in einer Datei gespeicherten Zertifikats. Die Informationen des privaten Schlüssels werden durch ein Hardwarekryptografiemodul geschützt, und der Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](../secgloss/c-gly.md) CSP) und der [*Schlüsselcontainer*](../secgloss/k-gly.md) werden durch den Namen angegeben. Dieser Befehl ist nützlich, wenn das Zertifikat nicht ordnungsgemäß installiert ist.

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

[SignTool gibt](signtool.md) den Befehlszeilentext zurück, der das Ergebnis des Signaturvorgang angibt. Darüber hinaus gibt SignTool den Exitcode 0 (null) für die erfolgreiche Ausführung zurück, einen für die fehlgeschlagene Ausführung und zwei für die Ausführung, die mit Warnungen abgeschlossen wurde.

Informationen zum Überprüfen der Signatur einer Datei finden Sie unter Verwenden von SignTool zum Überprüfen [einer Dateisignatur.](using-signtool-to-verify-a-file-signature.md) Informationen zum Hinzufügen eines Zeitstempels, wenn die Datei bereits signiert wurde, finden Sie unter Hinzufügen von [Zeitstempeln zu zuvor signierten Dateien.](adding-time-stamps-to-previously-signed-files.md) Weitere Informationen zu [SignTool finden Sie](signtool.md)unter [SignTool](signtool.md).

 

 

---
description: Erläutert, wie SignTool verwendet wird, um eine Datei zu signieren.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Signieren einer Datei mithilfe von SignTool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089026cde629278e5c6ac033164c2a9d26528917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130236"
---
# <a name="using-signtool-to-sign-a-file"></a>Signieren einer Datei mithilfe von SignTool

Mit dem folgenden Befehl wird die Datei mit dem Namen MyControl.exe unter Verwendung eines [*Zertifikats*](../secgloss/c-gly.md) signiert, das in einer PFX-Datei (Personal Information Exchange) gespeichert ist:

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

Mit dem folgenden Befehl wird die Datei mithilfe eines Zertifikats signiert, das in einer Kenn Wort geschützten PFX-Datei gespeichert ist:

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> Stellen Sie sicher, dass Sie das Kennwort richtig schützen.

 

Der folgende Befehl signiert und Zeitstempel für die Datei:

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> Informationen zum Zeitstempel einer Datei, nachdem Sie bereits signiert wurde, finden Sie unter [Hinzufügen von Zeitstempeln zu zuvor signierten Dateien](adding-time-stamps-to-previously-signed-files.md).

 

Mit dem folgenden Befehl wird die Datei mithilfe eines Zertifikats in "My Store" mit dem Antragsteller Namen "My Company Publisher" signiert:

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

Der folgende Befehl signiert ein ActiveX-Steuerelement und stellt Informationen bereit, die von Internet Explorer angezeigt werden, wenn der Benutzer aufgefordert wird, das-Steuerelement zu installieren:

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

Mit dem folgenden Befehl wird die Datei mithilfe eines Zertifikats signiert, dessen Informationen zum [*privaten Schlüssel*](../secgloss/p-gly.md) von einem Hardware kryptografiemodul geschützt werden. Nehmen Sie beispielsweise an, dass das Zertifikat mit dem Namen "My High-Value Certificate" einen privaten Schlüssel enthält, der in einem Hardware kryptografiemodul installiert ist, und dass das Zertifikat ordnungsgemäß installiert ist.

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

Mit dem folgenden Befehl wird die Datei mithilfe eines Zertifikats signiert, dessen Informationen zum [*privaten Schlüssel*](../secgloss/p-gly.md) von einem Hardware kryptografiemodul geschützt werden. Für den [*Zertifizierungs*](../secgloss/c-gly.md) stellen Speicher (ca) ist ein Computerspeicher angegeben.

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

Mit dem folgenden Befehl wird die Datei mithilfe eines Zertifikats signiert, das in einer Datei gespeichert ist. Die Informationen zum privaten Schlüssel werden durch ein Hardware kryptografiemodul geschützt, und der [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und der [*Schlüssel Container*](../secgloss/k-gly.md) werden anhand des Namens angegeben. Dieser Befehl ist nützlich, wenn das Zertifikat nicht ordnungsgemäß installiert ist.

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

[SignTool](signtool.md) gibt Befehlszeilen Text zurück, der das Ergebnis des Signatur Vorgangs angibt. Außerdem gibt SignTool den Exitcode 0 (null) für die erfolgreiche Ausführung zurück, einen für die fehlgeschlagene Ausführung und zwei für die Ausführung, die mit Warnungen abgeschlossen wurden.

Weitere Informationen zum Überprüfen der Signatur einer Datei finden [Sie unter Verwenden von SignTool zum Überprüfen einer Datei Signatur](using-signtool-to-verify-a-file-signature.md). Weitere Informationen zum Hinzufügen eines Zeitstempels, wenn die Datei bereits signiert wurde, finden [Sie unter Hinzufügen von Zeitstempeln zu zuvor signierten Dateien](adding-time-stamps-to-previously-signed-files.md). Weitere Informationen zu [SignTool](signtool.md)finden Sie unter [SignTool](signtool.md).

 

 

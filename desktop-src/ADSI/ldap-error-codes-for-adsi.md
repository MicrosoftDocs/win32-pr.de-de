---
title: LDAP-Fehler Codes für ADSI
description: Wenn ein LDAP-Server einen Fehler generiert und den Fehler an den Client übergibt, wird der Fehler dann vom LDAP-Client in eine Zeichenfolge übersetzt.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855284"
---
# <a name="ldap-error-codes-for-adsi"></a>LDAP-Fehler Codes für ADSI

Wenn ein LDAP-Server einen Fehler generiert und den Fehler an den Client übergibt, wird der Fehler dann vom LDAP-Client in eine Zeichenfolge übersetzt.

Diese Methode ähnelt den [Win32-Fehlercodes für ADSI](win32-error-codes-for-adsi.md). In diesem Beispiel ist der Client Fehlercode der Win32-Fehler 0x80072020.

**So bestimmen Sie die LDAP-Fehlercodes für ADSI**

1.  Legen Sie den 8007 aus dem Win32-Fehlercode ab. Im Beispiel ist der verbleibende Hexadezimalwert 2020.
2.  Konvertiert den verbleibenden Hexadezimalwert in einen Dezimalwert. Im Beispiel wird der verbleibende Hexadezimalwert 2020 in den Dezimalwert 8224 konvertiert.
3.  Suchen Sie in der Datei "Winerror. h" nach der Definition des Dezimal Werts. Im Beispiel entspricht 8224l dem Fehler Fehler DS- **\_ \_ Vorgangs \_ Fehler**.
4.  Ersetzen Sie den Präfix **Fehler \_ DS** durch **LDAP \_**. Im Beispiel ist die neue Definition LDAP- **\_ Vorgangs \_ Fehler**.
5.  Suchen Sie in der Datei winldap. h nach dem Wert der LDAP-Fehler Definition. Im Beispiel lautet der Wert von **LDAP- \_ Vorgangs \_ Fehler** in der Datei "winldap. h" 0x01.

 

 





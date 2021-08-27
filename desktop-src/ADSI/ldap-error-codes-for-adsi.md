---
title: LDAP-Fehlercodes für ADSI
description: Wenn ein LDAP-Server einen Fehler generiert und den Fehler an den Client übergibt, wird der Fehler vom LDAP-Client in eine Zeichenfolge übersetzt.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6280784d8bf9fc9c692cb38f1ca2d0e76646b1d2a3d464e516f03e7ac682fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005510"
---
# <a name="ldap-error-codes-for-adsi"></a>LDAP-Fehlercodes für ADSI

Wenn ein LDAP-Server einen Fehler generiert und den Fehler an den Client übergibt, wird der Fehler vom LDAP-Client in eine Zeichenfolge übersetzt.

Diese Methode ähnelt [Win32-Fehlercodes für ADSI.](win32-error-codes-for-adsi.md) In diesem Beispiel ist der Clientfehlercode der WIN32-Fehler 0x80072020.

**So bestimmen Sie die LDAP-Fehlercodes für ADSI**

1.  Löschen Sie 8007 aus dem WIN32-Fehlercode. Im Beispiel ist der verbleibende hexadezimale Wert 2020.
2.  Konvertieren Sie den verbleibenden Hexadezimalwert in einen Dezimalwert. Im Beispiel wird der verbleibende Hexadezimalwert 2020 in den Dezimalwert 8224 konvertiert.
3.  Suchen Sie in der Datei WinError.h nach der Definition des Dezimalwerts. Im Beispiel entspricht 8224L dem Fehler **ERROR \_ DS \_ OPERATIONS \_ ERROR**.
4.  Ersetzen Sie das Präfix **ERROR \_ DS** durch **\_ LDAP**. Im Beispiel lautet die neue Definition **LDAP \_ OPERATIONS \_ ERROR**.
5.  Suchen Sie in der Datei Winldap.h nach dem Wert der LDAP-Fehlerdefinition. Im Beispiel wird der Wert von **LDAP \_ OPERATIONS \_ ERROR** in der Datei Winldap.h 0x01.

 

 





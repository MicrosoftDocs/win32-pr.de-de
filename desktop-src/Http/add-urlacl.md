---
title: add urlacl
description: Reserviert die angegebene URL für Benutzer und Konten ohne Administratorrechte.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Hinzufügen von urlacl http
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "103961537"
---
# <a name="add-urlacl"></a>add urlacl

Reserviert die angegebene URL für Benutzer und Konten ohne Administratorrechte. Die freigegebene Zugriffs Steuerungs Liste (DACL) kann mithilfe eines Konto namens mit den Abhör-und delegatparametern oder mithilfe einer SDDL-Zeichenfolge (Security Deskriptor Definition Language) angegeben werden.

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[URL =] Zeichenfolge**
</dt> <dd>

Gibt die voll qualifizierte URL an.

</dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user =] Zeichenfolge**
</dt> <dd>

Gibt den Namen des Benutzers oder der Benutzergruppe an.

</dd> <dt>

<span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[lauschen = {Yes \| No}\]**
</dt> <dd>

Gibt einen der folgenden Werte an:

-   Ja: ermöglicht dem Benutzer das Registrieren von URLs. Dies ist der Standardwert.
-   Nein: verweigert dem Benutzer das Registrieren von URLs.

</dd> <dt>

<span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[Delegat = {Yes \| No}\]**
</dt> <dd>

Gibt einen der folgenden Werte an:

-   Ja: ermöglicht dem Benutzer das Delegieren von URLs.
-   Nein: verweigert dem Benutzer die Delegierung von URLs. Dies ist der Standardwert.

</dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] Zeichenfolge**
</dt> <dd>

Gibt die SDDL-Zeichenfolge an, die die DACL beschreibt.

</dd> </dl>

## <a name="examples"></a>Beispiele

* add urlacl url=https://+:80/MyUri user=DOMAIN\\ user

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no

 
## <a name="see-also"></a>Weitere Informationen

* [Netsh http-Befehle](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 
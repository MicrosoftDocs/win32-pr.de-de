---
title: add urlacl
description: Reserviert die angegebene URL für Benutzer und Konten ohne Administratorrechte.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- urlacl HTTP hinzufügen
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: e3f4c715df70255ede8bd9ca5fc23131102983f8a3aeeb25735d5fc81d5ad9b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638780"
---
# <a name="add-urlacl"></a>add urlacl

Reserviert die angegebene URL für Benutzer und Konten ohne Administratorrechte. Die DACL (Discretionary Access Control List) kann mithilfe eines Kontonamens mit den Listen- und Delegatparametern oder mithilfe einer SDDL-Zeichenfolge (Security Descriptor Definition Language) angegeben werden.

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url=] zeichenfolge**
</dt> <dd>

Gibt die vollqualifizierte URL an.

</dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user=] string**
</dt> <dd>

Gibt den Namen des Benutzers oder der Benutzergruppe an.

</dd> <dt>

<span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[listen={ja \| nein}\]**
</dt> <dd>

Gibt einen der folgenden Werte an:

-   ja: Ermöglicht dem Benutzer das Registrieren von URLs. Dies ist der Standardwert.
-   nein: Verweigert dem Benutzer die Registrierung von URLs.

</dd> <dt>

<span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate={yes \| no}\]**
</dt> <dd>

Gibt einen der folgenden Werte an:

-   ja: Ermöglicht dem Benutzer das Delegieren von URLs.
-   nein: Verweigert dem Benutzer das Delegieren von URLs. Dies ist der Standardwert.

</dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl=] string**
</dt> <dd>

Gibt die SDDL-Zeichenfolge an, die die DACL beschreibt.

</dd> </dl>

## <a name="examples"></a>Beispiele

* add urlacl url=https://+:80/MyUri user=DOMAIN\\ user

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no

 
## <a name="see-also"></a>Weitere Informationen

* [Netsh http-Befehle](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 
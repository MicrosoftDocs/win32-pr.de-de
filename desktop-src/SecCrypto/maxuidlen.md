---
description: Eine numerische Konstante, die die maximale Anzahl von Zeichen angibt, die von einigen Kryptografieanbietern von Microsoft beim Abrufen der Benutzer-ID verwendet werden.
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: Maxuidlen (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 199d8e697deba86ffe48d4f76501f2d9d3a6d4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347796"
---
# <a name="maxuidlen"></a>Maxuidlen

Maxuidlen ist eine numerische Konstante, die die maximale Anzahl von Zeichen angibt, die von einigen Kryptografieanbietern von Microsoft beim Abrufen der Benutzer-ID verwendet werden. maxuidlen ist in Wincrypt. h definiert.



| Konstante/Wert                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <dt>**Maxuidlen**</dt> <dt>64 (0x40)</dt> </dl> | Wenn der *pszcontainer* -Parameter der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion **null** ist, verwenden einige der Kryptografieanbieter von Microsoft den Anmelde Namen des aktuell angemeldeten Benutzers als Schlüssel Container Namen. Maxuidlen gibt die maximale Anzahl von Zeichen an, einschließlich des abschließenden **null** -Zeichens, das diese Anbieter für den Benutzernamen verwenden.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinCrypt. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[**Cpacquirecontext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 





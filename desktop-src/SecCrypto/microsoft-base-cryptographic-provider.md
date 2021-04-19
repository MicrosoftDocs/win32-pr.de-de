---
description: Der Kryptografieanbieter von Microsoft ist der erste Kryptografiedienstanbieter-Anbieter (kryptografischen Service Provider, CSP) und wird mit den kryptoapi-Versionen 1,0 und 2,0 verteilt. Dabei handelt es sich um einen allgemeinen Anbieter, der digitale Signaturen und Datenverschlüsselung unterstützt.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Kryptografieanbieter von Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc48060305337dd878dedcadca8cfed52bd2f34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350466"
---
# <a name="microsoft-base-cryptographic-provider"></a>Kryptografieanbieter von Microsoft

Der Kryptografieanbieter von Microsoft ist der erste [*Kryptografiedienstanbieter-Anbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) und wird mit den [*kryptoapi*](../secgloss/c-gly.md) -Versionen 1,0 und 2,0 verteilt. Dabei handelt es sich um einen allgemeinen Anbieter, der [*digitale Signaturen*](../secgloss/d-gly.md) und Datenverschlüsselung unterstützt.

Der RSA-Algorithmus für öffentliche Schlüssel wird für alle Vorgänge mit öffentlichem Schlüssel verwendet.

Um die Abwärtskompatibilität mit früheren Versionen zu gewährleisten, behält die neue Version des Anbieters die Bezeichnung Version 1,0 des Namens in Wincrypt. h bei. Die Version 2,0 dieses Anbieters wird jedoch zurzeit versendet. Um die tatsächliche Version des verwendeten Anbieters zu ermitteln, nennen Sie [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) mit dem *dwparam* -Argument, das auf die **PP- \_ Version** festgelegt ist. Wenn 0x0200 in *pbData* zurückgegeben wird, verfügen Sie über die Version 2,0.

|                |                     |
|----------------|---------------------|
| Anbietertyp: | **Prov \_ RSA \_ Full** |
| Anbieter Name: | **MS \_ DEF \_ Prov**   |



 

 

 

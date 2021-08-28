---
description: Der Microsoft Base Cryptographic Provider ist der anfängliche CSP-Anbieter (Cryptographic Service Provider) und wird mit den CryptoAPI-Versionen 1.0 und 2.0 verteilt. Es handelt sich um einen allgemeinen Anbieter, der digitale Signaturen und Datenverschlüsselung unterstützt.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Microsoft Base Cryptographic Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32082fc6cd7ec6d34bd994e3d3122e2b4c06eee290af8074cea0c183e5dd0116
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100700"
---
# <a name="microsoft-base-cryptographic-provider"></a>Microsoft Base Cryptographic Provider

Der Microsoft Base Cryptographic Provider ist der anfängliche [*CSP-Anbieter (Cryptographic Service Provider)*](../secgloss/c-gly.md) und wird mit [*den CryptoAPI-Versionen*](../secgloss/c-gly.md) 1.0 und 2.0 verteilt. Es handelt sich um einen allgemeinen Anbieter, der [*digitale Signaturen*](../secgloss/d-gly.md) und Datenverschlüsselung unterstützt.

Der RSA-Algorithmus für öffentliche Schlüssel wird für alle Vorgänge mit öffentlichem Schlüssel verwendet.

Um die Abwärtskompatibilität mit früheren Versionen zu gewährleisten, behält die neue Version des Anbieters die Version 1.0-Bezeichnung des Namens in Wincrypt.h bei. Version 2.0 dieses Anbieters wird derzeit jedoch ausgeliefert. Um die tatsächliche Version des verwendeten Anbieters zu bestimmen, rufen [**Sie CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) auf, wobei das *dwParam-Argument* auf **PP \_ VERSION** festgelegt ist. Wenn 0x0200 in *pbData* zurückgegeben wird, verfügen Sie über Version 2.0.

|                   | Wert            |
|-------------------|------------------|
| **Anbietertyp** | PROV \_ RSA \_ FULL  |
| **Anbietername** | MS \_ DEF \_ PROV    |



 

 

 

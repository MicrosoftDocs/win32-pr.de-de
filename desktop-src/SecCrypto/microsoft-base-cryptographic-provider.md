---
description: Der Microsoft Base Cryptographic Provider ist der erste Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) und wird mit den CryptoAPI-Versionen 1.0 und 2.0 verteilt. Es ist ein allgemeiner Anbieter, der digitale Signaturen und Datenverschlüsselung unterstützt.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Microsoft Base Cryptographic Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53bd4b2f7faf140e57d25b54d3161b47dcaf740
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581888"
---
# <a name="microsoft-base-cryptographic-provider"></a>Microsoft Base Cryptographic Provider

Der Microsoft Base Cryptographic Provider ist der erste Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](../secgloss/c-gly.md) CSP) und wird mit [*den CryptoAPI-Versionen*](../secgloss/c-gly.md) 1.0 und 2.0 verteilt. Es ist ein allgemeiner Anbieter, der digitale [*Signaturen und*](../secgloss/d-gly.md) Datenverschlüsselung unterstützt.

Der RSA-Algorithmus für öffentliche Schlüssel wird für alle Vorgänge mit öffentlichem Schlüssel verwendet.

Zur Aufrechterhaltung der Abwärtskompatibilität mit früheren Versionen behält die neue Version des Anbieters die Version 1.0-Bezeichnung des Namens in Wincrypt.h bei. Version 2.0 dieses Anbieters wird derzeit jedoch im Versand verfügbar sein. Um die tatsächliche Version des zu verwendenden Anbieters zu ermitteln, rufen Sie [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) auf, und legen Sie dabei das *argument dwParam* auf **PP VERSION \_ fest.** Wenn 0x0200 in *pbData* zurückgegeben wird, verfügen Sie über Version 2.0.

|                   | Wert            |
|-------------------|------------------|
| **Anbietertyp** | PROV \_ RSA \_ FULL  |
| **Anbietername** | MS \_ DEF \_ PROV    |



 

 

 

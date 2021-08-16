---
description: Bei allen Beispielen in der Cryptography SDK-Dokumentation wird davon ausgegangen, dass sie die folgenden \# \# Compilerdirektiven enthalten und definieren.
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#includes und #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dbab2a3c33b510df99c9d2e0fa292af53c96fcc471dfe8180d9d4be06b3a5b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774275"
---
# <a name="includes-and-defines"></a>\#includes and \# defines

Bei allen Beispielen in der Cryptography SDK-Dokumentation wird davon ausgegangen, dass sie die folgenden Compilerdirektiven **\# enthalten** und **\# definieren.**


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



Darüber hinaus muss die **\_ WIN32 \_ WINNT-Konstante** entsprechend definiert werden. Weitere Informationen zu **\_ WIN32 \_ WINNT** finden Sie unter [Verwenden der Windows Header.](../winprog/using-the-windows-headers.md)

 

 

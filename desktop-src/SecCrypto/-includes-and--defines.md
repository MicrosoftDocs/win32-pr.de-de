---
description: Bei allen Beispielen in der Cryptography SDK-Dokumentation wird davon ausgegangen, dass Sie die folgenden \# \# Compilerdirektiven einschließen und definieren.
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#umfasst und #Defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9834fd8103b9fd28a01e416bd1df8b03fb7ad680
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364994"
---
# <a name="includes-and-defines"></a>\#umfasst und \# definiert

Bei allen Beispielen in der Cryptography SDK-Dokumentation wird davon ausgegangen, dass Sie die folgenden Compilerdirektiven **\# einschließen** und **\# definieren** .


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



Außerdem muss die **\_ Win32- \_ Winnt** -Konstante entsprechend definiert werden. Weitere Informationen zu **\_ Win32 \_ Winnt** finden Sie unter [Verwenden der Windows-Header](../winprog/using-the-windows-headers.md).

 

 

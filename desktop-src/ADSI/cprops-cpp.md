---
title: CPROPS. Cpp
description: In der Beispielanbieterkomponente finden Sie ein Beispiel für eine Eigenschaftencacheimplementierung in cprops.cpp. Die unterstützten Methoden sind in der folgenden Tabelle aufgeführt.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66394b7375779f50a97505128178ec35106187c076ca5d6741375a7f71b8ec46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428999"
---
# <a name="cpropscpp"></a>CPROPS. Cpp

In der Beispielanbieterkomponente finden Sie ein Beispiel für eine Eigenschaftencacheimplementierung in cprops.cpp. Die unterstützten Methoden sind in der folgenden Tabelle aufgeführt.



| Methode                                           | Beschreibung                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **CPropertyCache::addproperty**                  | Erweitern Sie den Eigenschaftencache, indem Sie einen neuen hinzufügen.                                                                      |
| **CPropertyCache::updateproperty**               | Suchen Sie die Eigenschaft, geben Sie ihren Inhalt frei, und verwenden Sie stattdessen neue Werte. markieren Sie dann den geänderten Cache für diese Eigenschaft. |
| **CPropertyCache::findproperty**                 | Suchen Sie diese Eigenschaft nach Namen. speichern Sie den Index.                                                                      |
| **CPropertyCache::getproperty**                  | Suchen Sie die -Eigenschaft im Cache, falls verfügbar, andernfalls **Rufen Sie GetInfo auf.** Legen Sie den Index fest, und kopieren Sie die neuen Werte.  |
| **CPropertyCache::p utproperty**                  | Suchen Sie die -Eigenschaft. Geben Sie frei, was dort war, und geben Sie neue Werte ein.                                                       |
| **CPropertyCache::CPropertyCache**               | Standardkonstruktor.                                                                                               |
| **CPropertyCache::~CPropertyCache**              | Standard-Destruktor.                                                                                                |
| **CPropertyCache::createpropertycache**          | Erstellen Sie den Cache.                                                                                                   |
| **CPropertyCache::unboundgetproperty**           | Suchen Sie die -Eigenschaft im Cache, und legen Sie sie auf diese Werte fest.                                                          |
| **CPropertyCache::SampleDSMarshallProperties**   | Marshallen Sie Eigenschaftsdaten und -werte.                                                                                   |
| **CPropertyCache::marshallproperty**             | Marshallen einer Eigenschaft.                                                                                                 |
| **CPropertyCache::SampleDSUnMarshallProperties** | Unmarshal-Eigenschaftsdaten und -werte.                                                                                 |
| **CPropertyCache::unmarshallproperty**           | Entmarshalieren einer Eigenschaft.                                                                                               |



 

 

 





---
title: Transaktionsflags
description: Ein Objekt kann entweder im direkten oder im transaktionsorientierten Modus geöffnet werden.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a3f389def4bdbb9d0cabf92500b316ae354878ec5f790b44e9f01121aeb57a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886782"
---
# <a name="transaction-flags"></a>Transaktionsflags

Ein Objekt kann entweder im direkten oder im transaktionsorientierten Modus geöffnet werden. Wenn ein Objekt im direkten Modus geöffnet wird, werden Änderungen sofort und dauerhaft vorgenommen. Wenn ein Objekt im transaktionsorientierten Modus geöffnet wird, werden Änderungen gepuffert, sodass sie nach Abschluss der Bearbeitung explizit ausgeführt oder rückgängig machen werden können. Änderungen, für die ein Committed vorgenommen wurde, werden im Objekt gespeichert, während zurückgedrehte Änderungen verworfen werden. Der direkte Modus ist der Standardzugriffsmodus.

Der Transaktionsmodus ist für ein übergeordnetes Speicherobjekt nicht erforderlich, um ihn für ein geschachtelte Element zu verwenden. Eine Transaktion für ein geschachtelte Element ist jedoch innerhalb der Transaktion für das übergeordnete Speicherobjekt geschachtelt. Aus diesem Grund kann für Änderungen, die an einem untergeordneten Objekt vorgenommen werden, erst dann ein Committed für die änderungen an dem übergeordneten Objekt vorgenommen werden, wenn ein Committed für beide vorgenommen wurde. Beide bleiben so lange ohneComcommitted, bis das Stammspeicherobjekt (das übergeordnete Objekt der obersten Ebene) tatsächlich auf den Datenträger geschrieben wird. Anders ausgedrückt: Die Änderungen verschieben sich nach außen: Innere Objekte veröffentlichen Änderungen an den Transaktionen ihrer unmittelbaren Container.

 

 





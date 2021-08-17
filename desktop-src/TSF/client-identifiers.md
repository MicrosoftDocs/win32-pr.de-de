---
title: Clientbezeichner
description: Clientbezeichner
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- Textdienstframework (TSF), Clientbezeichner
- TSF (Textdienstframework),Clientbezeichner
- Textdienste, Clientbezeichner
- TSF-fähige Anwendungen, Clientbezeichner
- Clientbezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f37b230eed1f47ad3e31a5831bddaf8634837c1173806deb084c1e3a4d08790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117953908"
---
# <a name="client-identifiers"></a>Clientbezeichner

## <a name="applications"></a>Anwendungen

Eine Anwendung ruft ihren Clientbezeichner ab, indem [sie ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)aufruft.

## <a name="text-services"></a>Textdienste

Ein Textdienst ruft seinen Clientbezeichner ab, wenn die [ITfTextInputProcessor::Activate-Methode](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) des Textdiensts aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




